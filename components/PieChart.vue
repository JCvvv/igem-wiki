<template>
  <!-- 饼图 -->
  <div id="piechart"
       class="col-lg-6"
       data-aos="slide-left"
       data-aos-duration="1000">
    <Pie :chart-options="chartOptions"
         :chart-data="chartData" />
  </div>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'
import { Pie } from 'vue-chartjs/legacy'
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  ArcElement,
  CategoryScale
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, ArcElement, CategoryScale)

export default {
  name: 'PieChart',
  components: { Pie },
  data () {
    return {
      offset: 60,
      spacing: 30,
      rotation: 0,
      duration: 4000,
    }
  },
  computed: {
    chartData () {
      return {
        labels: ['Other', 'Lung', 'Breast', 'Colorectum', 'Prostate', 'Stomach', 'Liver', 'Esophagus', 'Cervix uteri', 'Thyroid', 'Bladder'],
        datasets: [
          {
            backgroundColor: ["#3417c6", "#735ce6", "#58646c", "#a2e8cc", "#2ae89b", "#7ca9f7", "#1e6cf7", "#7d8d99", "#2a2f33"],
            data: [{ label: 'Other', value: 36.6, count: "366" },
            { label: 'Lung', value: 11.6, count: "116" },
            { label: 'Breast', value: 11.6, count: "116" },
            { label: 'Colorectum', value: 10.2, count: "102" },
            { label: 'Prostate', value: 7.1, count: "71" },
            { label: 'Stomach', value: 5.7, count: "57" },
            { label: 'Liver', value: 4.7, count: "47" },
            { label: 'Esophagus', value: 3.2, count: "32" },
            { label: 'Cervix uteri', value: 3.2, count: "32" },
            { label: 'Thyroid', value: 3.1, count: "31" },
            { label: 'Bladder', value: 3.0, count: "30" }],
            hoverOffset: 40,
            spacing: this.spacing,
            offset: this.offset,
            rotation: this.rotation
          }
        ]
      }
    },
    chartOptions () {
      return {
        responsive: true,
        maintainAspectRatio: false,
        layout: {
          padding: 20
        },
        animation: {
          duration: this.duration,
          easing: "easeOutQuart"
        },
        plugins: {
          legend: {
            title: { text: "18.1 million new cases", display: true, font: { size: 12, weight: "bold" } },
            position: "right"
          },
          tooltip: {
            callbacks: {
              label: function (tooltipItem) {
                return tooltipItem.raw.value + "%"
              },
              title: function (tooltipItem) {
                return tooltipItem[0].raw.label
              }
            }
          }
        }
      }
    }
  },
  mounted () {
    AOS.init({});
    window.addEventListener("scroll", this.onScrollPie);
    window.addEventListener("load", () => {
      this.onScrollPie();
    });
  },
  beforeDestroy () {
    window.removeEventListener("scroll", this.onScrollPie);
  },
  methods: {
    onScrollPie: function () {
      const y = document.getElementById("piechart").getBoundingClientRect().y;
      const height = document.getElementById("piechart").getBoundingClientRect().height;
      if (y - window.innerHeight < -50 && y - window.innerHeight > -(height + window.innerHeight - 50)) {
        this.offset = 4;
        this.spacing = 4;
        this.rotation = -35;
        this.duration = 50;
      } else {
        this.duration = 4000;
        this.offset = 50;
        this.spacing = 30;
        this.rotation = 0;
      }
    }
  }
}
</script>
