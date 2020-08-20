<template>
  <div class="stats">
      <div class="table-responsive">
            <table class="table table-striped table-hover">
                <thead>
                <tr>
                    <th scope="col">#</th>
                    <th scope="col">Recovered</th>
                    <th scope="col">Deaths</th>
                    <th scope="col">Reported</th>
                </tr>
                </thead>
                <tbody>
                <tr :key="statistic" v-for="statistic in statistics">
                    <th scope="row">1</th>
                    <td>{{ statistic.recovered }}</td>
                    <td>{{ statistic.deaths }}</td>
                    <td>{{ statistic.confirmed }}</td>
                </tr>
                </tbody>
        </table>
</div>
  </div>
</template>

<script>
export default {
    name: "Stats",
    props: ['statistics']
}
</script>

<style>

</style>