<template>
  <v-data-table
    :headers="daysOfTheWeek"
    :items="days"
    :single-expand="singleExpand"
    :expanded.sync="expanded"
    item-key="name"
    show-expand
    class="elevation-1"
  >
    <template v-slot:top>
      <v-toolbar flat>
        <v-toolbar-title>Administrator Dashboard</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-switch
          v-model="singleExpand"
          label="Single expand"
          class="mt-2"
        ></v-switch>
      </v-toolbar>
    </template>
    <template v-slot:expanded-item="{ headers, item }">
      <td :colspan="headers.length">
        More info about {{ item.name }}
      </td>
    </template>
  </v-data-table>
</template>  
<script>
  export default {
    data () {
      return {
        expanded: [],
        singleExpand: false,
        daysOfTheWeek: [
          {
            text: 'Day',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Total(₦)', value: 'total' },
          { text: 'Delivery Price(₦)', value: 'deliveryprice' },
          { text: 'Markup Price(₦)', value: 'markupprice' },
          { text: 'Cost Price(₦)', value: 'costprice' },
          { text: 'Profits(₦)', value: 'profits' },
          { text: '', value: 'data-table-expand' },
        ],
        days: [
          {
            name: 'Monday 04/01/2021',
            total : 159,
            deliveryprice: 60000,
            markupprice: 34000,
            costprice: 15000,
            profits: '10000',
          },
          {
            name: 'Tuesday 05/01/2021',
            total: 237,
            deliveryprice: 45000,
            markupprice: 29000,
            costprice: 15000,
            profits: '15000',
          },
          {
            name: 'Wednesday 06/01/2021',
            total: 262,
            deliveryprice: 16540,
            markupprice: 23000,
            costprice: 15000,
            profits: '70000',
          },
          {
            name: 'Thursday 07/01/2021',
            total: 305,
            deliveryprice: 35950,
            markupprice: 19000,
            costprice: 15000,
            profits: '100000',
          },
          {
            name: 'Friday 08/01/2021',
            total: 356,
            deliveryprice: 28500,
            markupprice: 15000,
            costprice: 15000,
            profits: '150000',
          },
          {
            name: 'Saturday 09/01/2021',
            total: 375,
            deliveryprice: 35000,
            markupprice: 8000,
            costprice: 15000,
            profits: '180000',
          },
          {
            name: 'Sunday 10/01/2021',
            total: 392,
            deliveryprice: 20000,
            markupprice: 10000,
            costprice: 15000,
            profits: '200000',
          },
          {
            name: 'Tuesday 11/01/2021',
            total: 237,
            deliveryprice: 45000,
            markupprice: 29000,
            costprice: 15000,
            profits: '15000',
          },
          {
            name: 'Wednesday 12/01/2021',
            total: 262,
            deliveryprice: 16540,
            markupprice: 23000,
            costprice: 15000,
            profits: '70000',
          },
          {
            name: 'Thursday 13/01/2021',
            total: 305,
            deliveryprice: 35950,
            markupprice: 19000,
            costprice: 15000,
            profits: '100000',
          },
          {
            name: 'Friday 14/01/2021',
            total: 356,
            deliveryprice: 28500,
            markupprice: 15000,
            costprice: 15000,
            profits: '150000',
          },
          {
            name: 'Saturday 15/01/2021',
            total: 375,
            deliveryprice: 35000,
            markupprice: 8000,
            costprice: 15000,
            profits: '180000',
          },
          {
            name: 'Sunday 16/01/2021',
            total: 392,
            deliveryprice: 20000,
            markupprice: 10000,
            costprice: 15000,
            profits: '200000',
          }
        ],
      }
    },
  }
</script>