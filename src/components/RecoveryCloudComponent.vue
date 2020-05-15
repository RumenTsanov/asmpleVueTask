<template>
  <div id="recoveryCloudComponent" class="main-container">
    <aside>
      <p class="sub-head">Synch and Share</p>
      <h3>Acronis Cyber Disaster Recovery Cloud</h3>
      <p class="post-head">Just Updated</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </aside>
    <main>
      <div>
        <div class="row">
          <div
            class="col-12 col-sm-6 col-md-6 col-lg-6 col-xl-6"
            v-for="(obj, key) in sections"
            :key="key"
          >
            <font-awesome-icon class="icon" :icon="obj.icon" />
            <h6 class="title">{{obj.titile}}</h6>
            <p class="desc">{{obj.text}}</p>
          </div>
        </div>
      </div>
    </main>
    <a href="#">
      Learn More
      <font-awesome-icon class="arrow-icon" icon="arrow-right" />
    </a>
  </div>
</template>

<script>
export default {
  name: "RecoveryCloudComponent",
  data: () => ({
    sections: [
      {
        icon: "upload",
        titile: "AFP Connection to File Shares",
        text:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      },
      {
        icon: "upload",
        titile: "AFP Connection to File Shares",
        text:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      },
      {
        icon: "upload",
        titile: "AFP Connection to File Shares",
        text:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      },
      {
        icon: "upload",
        titile: "AFP Connection to File Shares",
        text:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      },
      {
        icon: "upload",
        titile: "AFP Connection to File Shares",
        text:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      },
      {
        icon: "upload",
        titile: "AFP Connection to File Shares",
        text:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      }
    ]
  })
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sub-head {
  font-size: 14px;
  color: #bdc1c6;
}
.post-head {
  color: #9bc225;
  font-size: 14px;
}
.main-container {
  padding: 5%;
}
aside {
  float: left;
  width: 33%;
  text-align: left;
  margin-right: 1%;
}
main {
  text-align: center;
}
.row {
  text-align: left;
}
.col-6 {
  padding: 1%;
}
.icon {
  font-size: 26px;
  margin-bottom: 15px;
  color: #3160ac;
}
.title {
  font-weight: bold;
}
.desc {
  font-size: 14px;
}
a {
  float: left;
  margin-top: -40px;
  font-size: 20px;
  font-weight: bold;
}
a:hover {
  text-decoration: none;
}

.arrow-icon {
  margin-bottom: -1px;
  margin-left: 5px;
  font-size: 16px;
}

@media (max-width: 1023px) {
  aside {
    float: none;
    width: 100%;
  }
  a {
    margin: 20px 0 20px 0;
  }
}
</style>
