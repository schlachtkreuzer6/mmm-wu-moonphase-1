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
                      apikey: 'abcde12345abcde12345abcde12345ab',
                      country: 'Switzerland',
                      city: 'Bern',
                      apiLang: 'EN',
				
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
				<br>This value is <b>REQUIRED</b>
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
	</tbody>
</table>
