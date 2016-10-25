<template>
	<aside class="main-sidebar">
    <!-- sidebar: style can be found in sidebar.less -->
    <section class="sidebar">
      <!-- Sidebar user panel (optional) -->
      <div class="user-panel">
        <div class="pull-left image">
          <img src="../../assets/AdminLTE/img/user2-160x160.jpg" class="img-circle" alt="User Image">
        </div>
        <div class="pull-left info">
          <p>{{info.user.username}}</p>
          <!-- Status -->
          <a href="#"><i class="fa fa-circle text-success"></i> 在线</a>
        </div>
      </div>

      <!-- Sidebar Menu -->
      <ul class="sidebar-menu">
        <li class="#" v-bind:class="{'active':c.active,'header':c.header}" v-for="c in info.menu.child"><a v-if="!c.header" href="{{c.link}}"><i class="fa fa-link"></i><span>{{c.name}}</span></a><span v-if="c.header">{{c.name}}</span></li>
      </ul>
      <!-- /.sidebar-menu -->
    </section>
    <!-- /.sidebar -->
  </aside>
</template>

<script>
export default {
  data () {
    return {
      info: {
        user: {
          username: 'fengche@126.com',
          logindate: '2016-10-25 20:02:00'
        },
        menu: {
          child: [
            {
              name: '菜单组',
              link: '#',
              active: false,
              header: true
            },
            {
              name: '菜单1',
              link: '#',
              active: true
            },
            {
              name: '菜单2',
              link: '#',
              active: false
            },
            {
              name: '菜单组',
              link: '#',
              active: false,
              header: true
            },
            {
              name: '菜单3',
              link: '#',
              active: false
            },
            {
              name: '菜单4',
              link: '#',
              active: false
            }
          ]
        }
      }
    }
  }
}
</script>