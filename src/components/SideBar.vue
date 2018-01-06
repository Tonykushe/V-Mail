<template>
  <aside class="sm-side">
    <div class="user-head">
      <img src="../assets/images/profile.jpg" alt="profile image">

      <div class="user-name">
        <h5>Tony Mugendi</h5>
        <span class="email-address">developer@tonymugendi.co.ke</span>
      </div>
    </div>

    <ul class="inbox-nav">
      <li :class="{ active: activeView == 'app-inbox'}">
        <a href="#" @click.prevent="navigate ('app-inbox', 'Inbox')">
          <i class="fas fa-inbox"></i>Inbox <span class="badge badge-danger float-right">?</span>
        </a>
      </li>

       <li :class="{ active: activeView == 'app-sent'}">
        <a href="#" @click.prevent="navigate ('app-sent', 'Sent')">
          <i class="fas fa-envelope"></i>Sent <span class="badge badge-secondary float-right">?</span>
        </a>
      </li>

       <li :class="{ active: activeView == 'app-important'}">
        <a href="#" @click.prevent="navigate ('app-important', 'Important')">
          <i class="fas fa-bookmark"></i>Important <span class="badge badge-warning float-right">?</span>
        </a>
      </li>

       <li :class="{ active: activeView == 'app-trash'}">
        <a href="#" @click.prevent="navigate ('app-trash', 'Trash')">
          <i class="fas fa-trash"></i>Trash <span class="badge badge-secondary float-right">?</span>
        </a>
      </li>

    </ul>
  </aside>
</template>

<<script>

  import { eventBus } from '../main'

export default {
  created (){
    eventBus.$on('changeView', (data) => {
      this.activeView = data.tag

    })
  },

  data (){
    return {
      activeView: 'app-inbox'
    }
  },

  methods: {
    navigate(newView, title) {
      eventBus.$emit('changeView', {
        tag: newView,
        title: title
      })
    }
  }
}
</script>







































<style scoped>
aside {
  display: table-cell;
  float: none;
  height: 100%;
  padding: 0;
  vertical-align: top;
}

.sm-side {
  background: none repeat scroll 0 0 #e5e8ef;
  border-radius: 0 0 4px 4px;
  width: 25%;
}

.sm-side .user-head {
  background: none repeat scroll 0 0 #00a8b3;
  color: #fff;
  height: 90px;
  padding: 20px;
}

.user-head img {
  float: left;
  border-radius: 50%;
}

.user-head .user-name h5 {
  font-size: 14px;
  font-weight: 300;
  margin-bottom: 0;
  cursor: default;
}

.user-head .user-name .email-address {
  color: #87e2e7;
  font-size: 12px;
  cursor: default;
}

ul.inbox-nav {
    display: inline-block;
    margin: 0;
    padding: 0;
    width: 100%;
}

ul.inbox-nav li {
  display: inline-block;
  line-height: 45px;
  width: 100%;
}

ul.inbox-nav li i {
    width: 25px;
    text-align: center;
}

ul.inbox-nav li a {
    color: #6a6a6a;
    display: inline-block;
    line-height: 45px;
    padding: 0 20px;
    width: 100%;
}

ul.inbox-nav li a:hover, ul.inbox-nav li.active a, ul.inbox-nav li a:focus {
    background: none repeat scroll 0 0 #d5d7de;
    color: #6a6a6a;
    text-decoration: none;
}

ul.inbox-nav li a i {
    color: #6a6a6a;
    font-size: 16px;
    padding-right: 30px;
}

ul.inbox-nav li a span.badge {
    margin-top: 13px;
    
}

</style>


