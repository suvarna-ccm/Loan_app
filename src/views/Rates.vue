<template>
    <v-main>
        <section>
         <h2>See Personalised Rates</h2>
  <div class="forms">
  <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th>
            Name
          </th>
          <th>
            Rates
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in Rates"
          :key="item.name"
        >
          <td>{{ item.name }}</td>
          <td>{{ item.rate }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
  </div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'Rates',
    data () {
      return {
        Rates: [
          {
            name: 'Home Loan',
            rate: 40,
          },
          {
            name: 'Maintainance Loan',
            rate: 30,
          }
        ]
      }
    }   



}
</script>

<style scoped>
th{text-align:center!important;}
</style>