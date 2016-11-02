# Module: mmm-wu-moonphase
The `mmm-wu-moonphase` module is a modules of the MagicMirror. This module displays the current moon phase, including a picture of the current moon and the percentage illumination.


## Installation

In your terminal, go to your MagicMirror's Module folder:
````
cd ~/MagicMirror/modules
git clone https://github.com/raffaelloit/mmm-wu-moonphase.git
````

Configure the module in your `config.js` file.

## Using the module

Get und set your API from wunderground.com and set your location and preferred language.

Now add the module to the modules array in the `config/config.js` file:
````javascript
modules: [
        {
                module: 'mmm-wu-moon-phases',
                header: 'Current Moon Phase',   // optionally you can add a header to this block
                position: 'top_right',  // this can be any of the regions.   
		              config: {
                      // See 'Configuration options' for more information.
                      apikey: 'abcde12345abcde12345abcde12345ab', // your API-Key from wunderground.org
                      country: 'Switzerland', // see exaple under: https://www.wunderground.com/weather/api/d/docs?d=data/astronomy
                      city: 'Bern', // same here like country
                      apiLang: 'EN', // Default englisch, see other language code under: https://www.wunderground.com/weather/api/d/docs?d=language-support
				
                }
        },
]
````

## Configuration options

The following properties can be configured:


<table width="100%">
	<!-- why, markdown... -->
	<thead>
		<tr>
			<th>Option</th>
			<th width="100%">Description</th>
		</tr>
	<thead>
	<tbody>	
		<tr>
			<td><code>apikey</code></td>
			<td>The <a href="https://www.wunderground.com/" target="_blank">Weatherunderground</a> API key, which can be obtained by creating an Weather Underground account.<br>
				<br> This value is <b>REQUIRED</b>
			</td>
		</tr>
		<tr>
			<td><code>country</code></td>
			<td>Search your city under <a href="https://www.wunderground.com">Weather Underground</a> <b>This will override the default value <code>Switzerland</code>.<br>
				<br><b>Example:</b> <code>United Kingdom</code>
				<br><b>Default value:</b> <code>Switzerland</code><br>
				<br> This value is <b>REQUIRED</b>
			</td>
		</tr>
		<tr>
			<td><code>city</code></td>
			<td>Search your city under  <a href="https://www.wunderground.com">Weather Underground</a> <b>This will override the default value <code>Bern</code>.<br>
				<br><b>Example:</b> <code>London</code>
				<br><b>Default value:</b> <code>Bern</code><br>
				<br> This value is <b>REQUIRED</b>
			</td>
		</tr>
		<tr>
			<td><code>apiLang</code></td>
			<td>The apiLang define the language of the json query. See <a href="https://www.wunderground.com/weather/api/d/docs?d=language-support">Weather Underground language support</a><br>
				<br><b>Possible values:</b> <code>DL</code>
				<br><b>Default value:</b> <code>EN</code>
			</td>
		</tr>
		<tr>
			<td><code>updateInterval</code></td>
			<td>How often does the content needs to be fetched? (Milliseconds)<br>
				<br><b>Default value:</b> <code>10800000</code> (every 3 houres)
			</td>
		</tr>
		<tr>
			<td><code>animationSpeed</code></td>
			<td>Speed of the update animation. (Milliseconds)<br>
				<br><b>Default value:</b> <code>1000</code> (1 seconds)
			</td>
		</tr>
		<tr>
			<td><code>initialLoadDelay</code></td>
			<td>The initial delay before loading. If you have multiple modules that use the same API key, you might want to delay one of the requests. (Milliseconds)<br>
				<br><b>Default value:</b>  <code>0</code> (0 seconds)
			</td>
		</tr>
		<tr>
			<td><code>retryDelay</code></td>
			<td>The delay before retrying after a request failure. (Milliseconds)<br>
				<br><b>Default value:</b>  <code>2500</code> (2.5 seconds)
			</td>
		</tr>
		<tr>
			<td><code>apiBase</code></td>
			<td>The Weather Underground  base URL.<br>
				<br><b>Default value:</b> <code>'http://api.wunderground.com/api'</code>
			</td>
		</tr>
		<tr>
			<td><code>moonEndpoint</code></td>
			<td>The Weather Underground API endPoint.<br>
				<br><b>Default value:</b>  <code>'.json'</code>
			</td>
		</tr>
	</tbody>
</table>
