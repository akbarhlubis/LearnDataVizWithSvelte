<script>
import * as d3 from "d3";
  import { getScatterData, getTimelineData } from "./data/data";
  import { get } from "svelte/store";

// Definisi variabel untuk parsing datanya
const parseData = d3.timeParse("%m/%d/%Y");
const dateAccessor = d => parseData(d.date);
const temperatureAccessor = d => d.temperature;
const humidityAccessor = d => d.humidity;

// Mengambil (get) data untuk di timeline dan scatternya
const getData = () => ({
  timeline: getTimelineData,
  scatter: getScatterData
})

// definsikan ke variabel baru
let data = getData();

console.log("getData")
</script>

<main>

</main>