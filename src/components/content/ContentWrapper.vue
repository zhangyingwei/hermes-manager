<template>
	<div class="content-wrapper">
    <!-- Content Header (Page header) -->
    <section class="content-header">
      <h1>
        {{info.page.name}}
        <small>{{info.page.desc}}</small>
      </h1>
    </section>

    <!-- Main content -->
    <section class="content">

      <!-- Your Page Content Here -->

    </section>
    <!-- /.content -->
  </div>
  <!-- /.content-wrapper -->
</template>

<script>
export default {
  data () {
    return {
      info: {
        page: {
          name: '首页',
          desc: '这里是首页'
        }
      }
    }
  }
}
</script>