<template>
  <v-data-table
    :headers="Total"
    :items="total"
    item-key="name"
    class="elevation-1"
  >
    <template v-slot:top>
      <v-toolbar flat>
        <v-toolbar-title>Total Table</v-toolbar-title>
      </v-toolbar>
    </template>
  </v-data-table>
</template>  
<script>
  export default {
    data () {
      return {
        Total: [
          {
            text: 'Total',
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
        total: [
          {
            name: 'Total',
            total : 159,
            deliveryprice: 60000,
            markupprice: 34000,
            costprice: 15000,
            profits: '10000',
          },
        ],
      }
    },
  }
</script>