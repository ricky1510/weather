<script>
	import { onMount } from "svelte";
	import Day from 'Components/Day/index.svelte';
	import DayOverlay from 'Components/DayOverlay/index.svelte';
	import Sun from 'Components/Sun/index.svelte';
	import Cloud from 'Components/Cloud/index.svelte';
	import Cloud2 from 'Components/Cloud2/index.svelte';

	const days = [
		{
			"time":1590897600,
			"summary":"Clear throughout the day.",
			"icon":"clear-day",
			"sunriseTime":1590916320,
			"sunsetTime":1590970500,
			"moonPhase":0.32,
			"precipIntensity":0.0004,
			"precipIntensityMax":0.0019,
			"precipIntensityMaxTime":1590955140,
			"precipProbability":0.04,
			"precipType":"rain",
			"temperatureHigh":63.17,
			"temperatureHighTime":1590958020,
			"temperatureLow":49.66,
			"temperatureLowTime":1591002180,
			"apparentTemperatureHigh":62.67,
			"apparentTemperatureHighTime":1590958020,
			"apparentTemperatureLow":50.15,
			"apparentTemperatureLowTime":1591002180,
			"dewPoint":38.28,
			"humidity":0.43,
			"pressure":1015.3,
			"windSpeed":11.14,
			"windGust":23.66,
			"windGustTime":1590933120,
			"windBearing":321,
			"cloudCover":0.12,
			"uvIndex":8,
			"uvIndexTime":1590943740,
			"visibility":10,
			"ozone":350.5,
			"temperatureMin":56.24,
			"temperatureMinTime":1590984000,
			"temperatureMax":68.63,
			"temperatureMaxTime":1590897600,
			"apparentTemperatureMin":56.73,
			"apparentTemperatureMinTime":1590984000,
			"apparentTemperatureMax":68.13,
			"apparentTemperatureMaxTime":1590897600
		},
		{
			"time":1590984000,
			"summary":"Partly cloudy throughout the day.",
			"icon":"partly-cloudy-day",
			"sunriseTime":1591002660,
			"sunsetTime":1591056960,
			"moonPhase":0.36,
			"precipIntensity":0.0032,
			"precipIntensityMax":0.0139,
			"precipIntensityMaxTime":1591035540,
			"precipProbability":0.27,
			"precipType":"rain",
			"temperatureHigh":63.57,
			"temperatureHighTime":1591039260,
			"temperatureLow":53.02,
			"temperatureLowTime":1591087800,
			"apparentTemperatureHigh":63.07,
			"apparentTemperatureHighTime":1591039260,
			"apparentTemperatureLow":53.51,
			"apparentTemperatureLowTime":1591087800,
			"dewPoint":35.13,
			"humidity":0.44,
			"pressure":1019.4,
			"windSpeed":5.48,
			"windGust":18.56,
			"windGustTime":1590984000,
			"windBearing":306,
			"cloudCover":0.34,
			"uvIndex":6,
			"uvIndexTime":1591026420,
			"visibility":10,
			"ozone":389.3,
			"temperatureMin":49.66,
			"temperatureMinTime":1591002180,
			"temperatureMax":63.57,
			"temperatureMaxTime":1591039260,
			"apparentTemperatureMin":50.15,
			"apparentTemperatureMinTime":1591002180,
			"apparentTemperatureMax":63.07,
			"apparentTemperatureMaxTime":1591039260
		},
		{
			"time":1591070400,
			"summary":"Partly cloudy throughout the day.",
			"icon":"partly-cloudy-day",
			"sunriseTime":1591089060,
			"sunsetTime":1591143420,
			"moonPhase":0.4,
			"precipIntensity":0.0002,
			"precipIntensityMax":0.0011,
			"precipIntensityMaxTime":1591110000,
			"precipProbability":0.08,
			"precipType":"rain",
			"temperatureHigh":68.65,
			"temperatureHighTime":1591130100,
			"temperatureLow":60.04,
			"temperatureLowTime":1591175040,
			"apparentTemperatureHigh":68.15,
			"apparentTemperatureHighTime":1591130100,
			"apparentTemperatureLow":60.53,
			"apparentTemperatureLowTime":1591175040,
			"dewPoint":43.71,
			"humidity":0.53,
			"pressure":1014.7,
			"windSpeed":5.8,
			"windGust":14.57,
			"windGustTime":1591130160,
			"windBearing":230,
			"cloudCover":0.59,
			"uvIndex":6,
			"uvIndexTime":1591117080,
			"visibility":10,
			"ozone":356.6,
			"temperatureMin":53.02,
			"temperatureMinTime":1591087800,
			"temperatureMax":68.65,
			"temperatureMaxTime":1591130100,
			"apparentTemperatureMin":53.51,
			"apparentTemperatureMinTime":1591087800,
			"apparentTemperatureMax":68.15,
			"apparentTemperatureMaxTime":1591130100
		},
		{
			"time":1591156800,
			"summary":"Rain in the evening and overnight.",
			"icon":"rain",
			"sunriseTime":1591175400,
			"sunsetTime":1591229880,
			"moonPhase":0.43,
			"precipIntensity":0.0053,
			"precipIntensityMax":0.0561,
			"precipIntensityMaxTime":1591239600,
			"precipProbability":0.59,
			"precipType":"rain",
			"temperatureHigh":77.24,
			"temperatureHighTime":1591218240,
			"temperatureLow":67.27,
			"temperatureLowTime":1591260660,
			"apparentTemperatureHigh":76.74,
			"apparentTemperatureHighTime":1591218240,
			"apparentTemperatureLow":67.76,
			"apparentTemperatureLowTime":1591260660,
			"dewPoint":51.18,
			"humidity":0.58,
			"pressure":1005.8,
			"windSpeed":6,
			"windGust":30.16,
			"windGustTime":1591240620,
			"windBearing":226,
			"cloudCover":0.83,
			"uvIndex":6,
			"uvIndexTime":1591201980,
			"visibility":10,
			"ozone":343.2,
			"temperatureMin":60.04,
			"temperatureMinTime":1591175040,
			"temperatureMax":77.24,
			"temperatureMaxTime":1591218240,
			"apparentTemperatureMin":60.53,
			"apparentTemperatureMinTime":1591175040,
			"apparentTemperatureMax":76.74,
			"apparentTemperatureMaxTime":1591218240
		},
		{
			"time":1591243200,
			"summary":"Clear throughout the day.",
			"icon":"rain",
			"sunriseTime":1591261800,
			"sunsetTime":1591316280,
			"moonPhase":0.47,
			"precipIntensity":0.0012,
			"precipIntensityMax":0.0355,
			"precipIntensityMaxTime":1591243200,
			"precipProbability":0.54,
			"precipType":"rain",
			"temperatureHigh":79.08,
			"temperatureHighTime":1591298340,
			"temperatureLow":62.66,
			"temperatureLowTime":1591347720,
			"apparentTemperatureHigh":78.58,
			"apparentTemperatureHighTime":1591298340,
			"apparentTemperatureLow":63.15,
			"apparentTemperatureLowTime":1591347720,
			"dewPoint":51.48,
			"humidity":0.5,
			"pressure":1004.9,
			"windSpeed":10.57,
			"windGust":29.59,
			"windGustTime":1591243200,
			"windBearing":268,
			"cloudCover":0.34,
			"uvIndex":9,
			"uvIndexTime":1591289040,
			"visibility":10,
			"ozone":335.5,
			"temperatureMin":67.27,
			"temperatureMinTime":1591260660,
			"temperatureMax":79.08,
			"temperatureMaxTime":1591298340,
			"apparentTemperatureMin":67.76,
			"apparentTemperatureMinTime":1591260660,
			"apparentTemperatureMax":78.58,
			"apparentTemperatureMaxTime":1591298340
		},
		{
			"time":1591329600,
			"summary":"Clear throughout the day.",
			"icon":"clear-day",
			"sunriseTime":1591348200,
			"sunsetTime":1591402740,
			"moonPhase":0.51,
			"precipIntensity":0.0001,
			"precipIntensityMax":0.0003,
			"precipIntensityMaxTime":1591346160,
			"precipProbability":0.01,
			"precipType":"rain",
			"temperatureHigh":79.36,
			"temperatureHighTime":1591388340,
			"temperatureLow":65.72,
			"temperatureLowTime":1591431780,
			"apparentTemperatureHigh":78.86,
			"apparentTemperatureHighTime":1591388340,
			"apparentTemperatureLow":66.21,
			"apparentTemperatureLowTime":1591431780,
			"dewPoint":45,
			"humidity":0.41,
			"pressure":1013.9,
			"windSpeed":6.03,
			"windGust":26.41,
			"windGustTime":1591416000,
			"windBearing":271,
			"cloudCover":0.14,
			"uvIndex":8,
			"uvIndexTime":1591375380,
			"visibility":10,
			"ozone":328.4,
			"temperatureMin":62.66,
			"temperatureMinTime":1591347720,
			"temperatureMax":79.36,
			"temperatureMaxTime":1591388340,
			"apparentTemperatureMin":63.15,
			"apparentTemperatureMinTime":1591347720,
			"apparentTemperatureMax":78.86,
			"apparentTemperatureMaxTime":1591388340
		}
	]

	function animateCelcius(day, duration) {
		let start = celcius; 
		let end = Math.round((day.apparentTemperatureHigh - 30) / 2);
		let range = end - start;
		let current = start;
		let increment = end > start? 1 : -1;
		let stepTime = Math.abs(Math.floor(duration / range));
		let timer = setInterval(function() {
			current += increment;
			celcius = current;	
			if (current == end || current <= 0) {
				clearInterval(timer);
			}
		}, stepTime);
	}

	function handleDayChange(event) {
		activeDay = event.detail.day;
	}
	let selectedDay;
	let activeDay = 0;
	$: vectorPosition = activeDay * 70 + 20;
	$: selectedDay = days[activeDay];
	let hour = 3;
	$: wind = Math.round(selectedDay.windSpeed * 1.6);
	$: humidity = Math.round(selectedDay.humidity * 100);
	let celcius = 0;
	
	$: if (selectedDay !== undefined) {
		animateCelcius(selectedDay, 800);	
	}
</script>


<svg width="0" height="0">
	<defs>
		<clipPath id="dayOverlayClip">
			<path transform="translate(0,{vectorPosition})" d="M200,140h5V0h-5V2.5A32.5,32.5,0,0,1,167.5,35H0v70H167.5A32.5,32.5,0,0,1,200,137.5Z" fill="#b05151"/>
		</clipPath>
	</defs>
</svg>
<div class="header">
	<div class="city__text">
		Heemskerk
	</div>
	<div class="header-date__text">
		Feb 03, Tuesday
	</div>
</div>
<div class="container">
	<div class="days__wrapper">
		{#each days as d, i}
			<Day i={i} on:changeDay={handleDayChange} timestamp={d.time} />
		{/each}
		<div class="overlay">
			<div class="days__wrapper">
				{#each days as d, i}
					<DayOverlay timestamp={d.time} />
				{/each}
			</div>
		</div>
	</div>
	<div class="day-detail__wrapper">
		<div class="left">
			<div class="degrees">
				<span class="degrees-number">{celcius}</span>
				<span class="degrees-celcius">°C</span>
			</div>
			<div class="selected-time">{selectedDay.summary}</div>
			<ul class="weather-details__list">
				<li class="weather-detail__li">
					<div class="icon__wrapper">
						<svg width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 144.74 134.15">
							<path d="M1,64.64A20.38,20.38,0,0,1,21.38,44.25a20.67,20.67,0,0,1,2.74.21,47,47,0,0,1,89.79-15.72c.55,0,1.11,0,1.67,0A28.16,28.16,0,0,1,116.76,85v0H20.16V85A20.37,20.37,0,0,1,1,64.64Z" fill="transparent" stroke="#fff" stroke-miterlimit="10" stroke-width="4"/>
							<path d="M46.05,115.49h0L34.82,94.23,23.61,115.31s-.05.08-.07.13l0,0h0a12.73,12.73,0,1,0,22.54,0Z" fill="#80d2ea"/>
							<path d="M83.64,115.49h0L72.41,94.23,61.2,115.31s-.05.08-.07.13l0,0h0a12.73,12.73,0,1,0,22.54,0Z" fill="#80d2ea"/>
							<path d="M121.23,115.49h0L110,94.23,98.79,115.31s-.05.08-.07.13l0,0h0a12.73,12.73,0,1,0,22.54,0Z" fill="#80d2ea"/>
						</svg>
					</div>
					{selectedDay.precipProbability * 100}% Precipitation
				</li>
				<li class="weather-detail__li">
					<div class="icon__wrapper">
						<svg width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 82 55">
							<line x1="2.5" y1="27.5" x2="70.5" y2="27.5" fill="none" stroke="#80d2ea" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
							<line x1="2.5" y1="18.5" x2="46.5" y2="18.5" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
							<line x1="2.5" y1="36.5" x2="50.5" y2="36.5" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
							<path d="M47.5,2.5a8,8,0,0,1,0,16" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
							<path d="M71.5,11.5a8,8,0,0,1,0,16" fill="none" stroke="#80d2ea" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
							<path d="M50.5,36.5a8,8,0,0,1,0,16" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
						</svg>
					</div>
					{wind} km/h Wind
				</li>
				<li class="weather-detail__li">
					<div class="icon__wrapper">
						<svg width="15" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 81.41 127.6">
							<path d="M75,68.89h0L40.83,4.27,6.75,68.32c-.08.13-.15.27-.22.41l-.09.16h0a38.7,38.7,0,1,0,73,18A38.44,38.44,0,0,0,75,68.89Z" fill="transparent" stroke="#fff" stroke-miterlimit="10" stroke-width="4"/>
							<path d="M58.63,77.58h0c2.54,3.39,3.47,8.75,2.06,14.27-2.11,8.22-8.6,13.65-14.49,12.14-.2,0-.38-.13-.57-.19h0c-.88,1.76-.25,3.88,1.2,4a10.78,10.78,0,0,0,4.14-.49c5-1.58,9.62-6.57,11.75-13.06,2.08-6.3,1.63-12.6-.63-17.15C61.33,75.57,59.51,75.8,58.63,77.58Z" fill="#80d2ea" stroke="#80d2ea" stroke-miterlimit="10" stroke-width="4"/>
						</svg>
					</div>
					{humidity}% Humidity
				</li>
			</ul>
		</div>
		<div class="day-selector">
			<div class="time-input__wrapper">
				<span class="filler m--start"></span>
				<input disabled type="range" min="1" max="6" bind:value={hour} class="slider" style="background: linear-gradient(to right, #6bedfd 0%, #6bedfd 40%, rgba(255, 255, 255, 0.5) 40%, rgba(255, 255, 255, 0.5) 100%)">
				<span class="filler m--end"></span>
			</div>
			<div class="times">
				<span>8:00 AM</span>
				<span>8:00 AM</span>
				<span>8:00 AM</span>
				<span>8:00 AM</span>
				<span>8:00 AM</span>
				<span>8:00 AM</span>
			</div>
		</div>
		<Sun type={selectedDay.icon} />
		<Cloud type={selectedDay.icon} />
		<Cloud2 type={selectedDay.icon} />
	</div>
</div>