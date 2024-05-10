<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <p>&copy; 2024 Vue.js Example</p>
                    <p>Carbon Footprint: {{ carbonFootprint }} kg CO2e</p>
                </div>
            </div>
        </div>
    </footer>
</template>
<script>

import axios from 'axios';

const CARBON_API_URL = 'https://api.carbonserviceprovider.com/carbon';
export default {
    name: 'Footer',
  data() {
    return {
      carbonFootprint: null
    };
  },
  async mounted() {
    try {
      const response = await axios.get(CARBON_API_URL);
      this.carbonFootprint = response.data.carbonFootprint;
    } catch (error) {
      console.error('Error fetching carbon footprint:', error);
    }
  }
};
</script>
<style>
footer {
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: #f8f9fa;
    padding: 20px 0;
    text-align: center;
}
</style>