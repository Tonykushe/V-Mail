<template>
  <aside class="sm-side">
    <div class="user-head">
      <img src="src/assets/images/profile.jpg" alt="profile image">

      <div class="user-name">
        <h5>Tony Mugendi</h5>
        <span class="email-address">developer@tonymugendi.co.ke</span>
      </div>
    </div>

    <ul class="inbox-nav">
      <li class="active">
        <a href="#">
          <i class="fas fa-inbox"></i>Inbox <span class="badge badge-danger pull-right">?</span>
        </a>
      </li>

       <li>
        <a href="#">
          <i class="fas fa-envelope"></i>Sent <span class="badge badge-secondary ">?</span>
        </a>
      </li>

       <li>
        <a href="#">
          <i class="fas fa-bookmark"></i>Important <span class="badge badge-warning pull-right">?</span>
        </a>
      </li>

       <li>
        <a href="#">
          <i class="fas fa-trash"></i>Trash <span class="badge badge-secondary pull-right">?</span>
        </a>
      </li>

    </ul>
  </aside>
</template>

<<script>
export default {
  
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


