<template>
  <div class="menu"
       :class="this.isOpened == true ? 'opened' : 'closed'">
    <div class="nav"
         style="user-select: none;">
      <a class="logo"
         @click="scrollToTop()">
        <img src="https://static.igem.wiki/teams/4776/wiki/smallicon.png"
             width="80"
             height="80" />
      </a>

      <p class="logo1">浙江大学 ZJUintl iGEM 团队</p>

      <div class="spacer"
           @click="clickOuside()"></div>
      <button class="burger hamburger hamburger--spin-r"
              :class="this.isOpened == true ? 'is-active' : ''"
              type="button"
              @click="handleMenu()">
        <span class="hamburger-box">
          <span class="hamburger-inner"></span>
        </span>
      </button>
    </div>
    <div class="content"
         @click="clickOuside()">
      <slot />
    </div>
    <aside style="user-select: none;">
      <ul class="w-full flex flex-col text-white pt-5">
        <li class="menu items"><a @click="pushRoute('/')">Home</a></li>
        <li class="menu items">
          <a @click="handleSubMenu('#project')">Project</a>
          <span class="arrow-right"></span>
        </li>
        <li class="menu items">
          <a @click="handleSubMenu('#team')">Team</a>
          <span class="arrow-right"></span>
        </li>
        <li class="menu items">
          <a @click="handleSubMenu('#WetLab')">Wet Lab</a>
          <span class="arrow-right"></span>
        </li>
        <li class="menu items">
          <a @click="handleSubMenu('#DryLab')">Dry Lab</a>
          <span class="arrow-right"></span>
        </li>
        <li class="menu items">
          <a @click="handleSubMenu('#HumanPractice')">Human Practice</a>
          <span class="arrow-right"></span>
        </li>

      </ul>
    </aside>

    <SubMenu id="team"
             selected="#team"
             className="submenu closed"
             :closeSubMenu="closeSubMenu">
      <li class="menu items"><a @click="pushRoute('/team')">Members</a></li>
      <li class="menu items"><a @click="pushRoute('/attributions')">Attributions</a></li>
      <li class="menu items"><a @click="pushRoute('/collaborations')">Collaborations</a></li>
      <li class="menu items"><a @click="pushRoute('/sponsors')">Sponsors</a></li>
    </SubMenu>

    <SubMenu id="project"
             selected="#project"
             className="submenu closed"
             :closeSubMenu="closeSubMenu">
      <li class="menu items"><a @click="pushRoute('/description')">Description</a></li>
      <li class="menu items"><a @click="pushRoute('/experiments')">Experiments</a></li>
      <li class="menu items"><a @click="pushRoute('/engineering')">Engineering</a></li>
      <li class="menu items"><a @click="pushRoute('/results')">Results</a></li>
      <li class="menu items"><a @click="pushRoute('/contribution')">Contribution</a></li>
    </SubMenu>

    <SubMenu id="HumanPractice"
             selected="#HumanPractice"
             className="submenu closed"
             :closeSubMenu="closeSubMenu">
      <li class="menu items"><a @click="pushRoute('/human-practices')">Human Practices</a></li>
      <li class="menu items"><a @click="pushRoute('/communication')">Education & Communication</a></li>
    </SubMenu>

    <SubMenu id="WetLab"
             selected="#WetLab"
             className="submenu closed"
             :closeSubMenu="closeSubMenu">
      <li class="menu items"><a @click="pushRoute('/education')">Experiments</a></li>
      <li class="menu items"><a @click="pushRoute('/inclusivity')">Protocols</a></li>
      <li class="menu items"><a @click="pushRoute('/sustainable')">Safety</a></li>
    </SubMenu>

    <SubMenu id="DryLab"
             selected="#WetLab"
             className="submenu closed"
             :closeSubMenu="closeSubMenu">
      <li class="menu items"><a @click="pushRoute('/proof-of-concept')">Software</a></li>
      <li class="menu items"><a @click="pushRoute('/implementation')">Model</a></li>

    </SubMenu>

  </div>
</template>

<script>
import SubMenu from './SubMenu.vue';
export default {
  data () {
    return {
      isOpened: false,
      subMenuId: "",
      options: {
        easing: [0.25, 0.1, 0.25, 1.0],
        force: true,
        cancelable: false,
        x: false,
        y: true
      },
    };
  },
  methods: {
    closeSubMenu: function () {
      this.$el.querySelector(this.subMenuId).className = "submenu closed";
      this.subMenuId = "";
    },
    openSubMenu: function (id) {
      this.subMenuId = id;
      this.$el.querySelector(this.subMenuId).className = "submenu opened";
    },
    handleMenu: function () {
      this.isOpened = !this.isOpened;
      if (this.subMenuId != "") this.closeSubMenu();
    },
    handleSubMenu: function (id) {
      if (this.subMenuId == id) this.closeSubMenu();
      else this.openSubMenu(id);
    },
    clickOuside: function () {
      if (this.isOpened) {
        this.handleMenu();
      }
    },
    pushRoute: function (to) {
      this.handleMenu();
      this.$router.push({ path: to });
    },
    scrollToTop: function () {
      this.$router.push({ path: "/" });
      this.$scrollTo("#top", 350, this.options);
    },
  },
  components: { SubMenu }
}
</script>
