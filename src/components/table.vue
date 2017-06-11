<template>
  <table>
    <thead ref="thead">
      <tr>
        <th>Month</th>
        <th>Saving</th>
      </tr>
    </thead>
    <tbody ref="tbody">
      <tr v-for="data in datas">
        <td>{{data.month}}</td>
        <td>{{data.saving}}</td>
      </tr>
    </tbody>
    <slot name="action"></slot>
  </table>
</template>

<script>
  export default {
    mounted () {
      console.log(this.$slots.action[0].tag)
    },
    data () {
      return {
        datas: [
          { 
            month: 1,
            saving: 12423
          },
          { 
            month: 1,
            saving: 12423
          },
          { 
            month: 1,
            saving: 12423
          },
          { 
            month: 1,
            saving: 12423
          }          
        ]
      }
    }
  }
</script>
