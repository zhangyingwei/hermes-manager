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
        <hermes-table></hermes-table>
    </section>
    <!-- /.content -->
  </div>
  <!-- /.content-wrapper -->
</template>

<script>
import HermesTable from './tabledemo/HermesTable'

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
          column: [
            {
              name: '编号',
              value: 'id',
              width: '60px'
            },
            {
              name: '任务',
              value: 'task'
            },
            {
              name: '完成程度',
              value: 'progress',
              class: ['progress', 'progress-xs']
            },
            {
              name: '标签',
              value: 'label',
              width: '80px'
            }
          ],
          data: [
            {
              id: 0,
              task: 'aaa',
              progress: 'bbbbb',
              label: '55%'
            }
          ]
        }
      }
    }
  }
}
</script>