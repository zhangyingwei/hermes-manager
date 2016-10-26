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
        <hermes-table v-bind:table-info="info.table" ></hermes-table>
    </section>
    <!-- /.content -->
  </div>
  <!-- /.content-wrapper -->
</template>

<script>
import HermesTable from '../selfcomps/HermesTable'

export default {
  components: {
    HermesTable
  },
  data () {
    return {
      info: {
        page: {
          name: '首页',
          desc: '这里是首页'
        },
        table: {
          name: '这是一个测试表格',
          col: [
            {
              name: '#',
              width: '10px'
            },
            {
              name: 'task'
            },
            {
              name: 'Progress'
            },
            {
              name: 'Label',
              width: '80px'
            }
          ]
        }
      }
    }
  }
}
</script>