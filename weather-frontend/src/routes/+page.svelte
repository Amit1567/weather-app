<!-- pages.svelte -->
<script>
  let city = "";
  let weatherData = {};

<<<<<<< HEAD
    async function getWeather() {
        const response = await fetch(`http://localhost:5000/api/weather?city=${city}`);
        weatherData = await response.json();
        console.log(weatherData);
        console.log(city);
    }
=======
  async function getWeather() {
    const response = await fetch(
      `http://localhost:5000/api/weather?city=${city}`
    );
    weatherData = await response.json();
    console.log(weatherData);
  }
>>>>>>> fe912cad26058f42c9ad95a1fbf49b01f7003b0f
</script>

<main>

<div class="container">
  <div class="input-container">
    <input type="text" bind:value={city} placeholder="Enter city" />
    <button on:click={getWeather}>Get Weather</button>
  </div>

<<<<<<< HEAD
    {#if Object.keys(weatherData).length > 0 }
        <div class="weather-info">
            <h2>Weather Information</h2>
            <h2> {weatherData.name}</h2>
            <p> Temperature: <b>  {weatherData.main.temp} °C</b></p>
            <p>Feels Like: <b>  {weatherData.main.feels_like} °C</b></p>
            <p>Min Temp: <b>  {weatherData.main.temp_min} °C</b></p>
            <p>Max Temp: <b>  {weatherData.main.temp_max}  °C</b></p>
            <p>Description: <b>  {weatherData.weather[0].description} </b></p>
            <p> Wind Speed: <b>  {weatherData.wind.speed} Km/hr </b></p>
            <p>Humidity: <b>  {weatherData.main.humidity} % </b></p>
            <p>Air Pressure: <b>  {weatherData.main.pressure} Pa </b></p>
=======
  {#if Object.keys(weatherData).length > 0}
    <div class="weather-info">
      <div class="temperature-info">
        <p class="temperature">{weatherData.main.temp}°</p>
        <p class="feels-like">Feels Like: {weatherData.main.feels_like}°C</p>
        <p class="city-info">{weatherData.name}</p>
      </div>
      <div class="weather-details">
        <div class="left-details">
          <p>Min Temp: {weatherData.main.temp_min}°C</p>
          <p>Max Temp: {weatherData.main.temp_max}°C</p>
          <p>Air Pressure: {weatherData.main.pressure} P</p>
>>>>>>> fe912cad26058f42c9ad95a1fbf49b01f7003b0f
        </div>
        <div class="right-details">
          <p>Humidity: {weatherData.main.humidity}%</p>
          <p>Wind Speed: {weatherData.wind.speed} Km/hr</p>
        </div>
      </div>
    </div>
  {/if}
</div>
</main>

<style>
<<<<<<< HEAD


main{
    font-family: Arial, sans-serif;
    background-image: url('../images/weatherimg.jpeg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    height: 100vh; 
    width: 100%;
    margin:0px; 
    padding: 0px;
    overflow: hidden;

}
.container {

    max-width: 400px;
    margin: 30px auto;
    text-align: center;
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.5); 
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3); 

}

h1{
    font-size: 24px;
}

input[type="text"] {
    width: 50%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
    outline: none;
}

button {
    background-color: #007BFF;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

.weather-info {
    margin-top: 20px;
}

.weather-info p {
    margin-bottom: 10px; 
}

=======
  /* Add your custom styles here */
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Free_Sky_%285596435888%29.jpg/800px-Free_Sky_%285596435888%29.jpg");
    background-color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .input-container {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }

  input[type="text"] {
    padding: 10px;
    margin-right: 10px;
    border-radius: 4px;
    border: 1px solid #ccc;
    font-size: 16px;
    width: 200px;
  }

  button {
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
  }

  .weather-info {
    text-align: center;
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    width: 100%;
  }

  .city-info {
    font-size: 1.1rem;
  }

  .temperature-info {
    flex: 1;
    text-align: center;
  }

  .temperature {
    font-size: 3rem;
    margin-bottom: 10px;
  }

  .feels-like {
    font-size: 1rem;
  }

  .weather-details {
    flex: 1;
    display: grid;
    grid-template-rows: repeat(2, 1fr);
    gap: 10px;
    text-align: left;
  }
>>>>>>> fe912cad26058f42c9ad95a1fbf49b01f7003b0f
</style>

