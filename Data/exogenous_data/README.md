This directory contains exogenous reference data that will be converted into normalized ESMC input data.
It contains the following directories:
	* csp :
	    * csp_ES-PT.xlsx:
		   * Excel file with the computation to merge the time series of CSP in Spain and in Portugal in order to have a time series for the Iberian Peninsula (ES-PT)
        * csp_to_compute.json
			* File giving the data of the csp plant to compute time series for regions with csp potential.
			  It was manually generated by comparing ENSPRESO maps for CSP potential at NUTS2 level with csp-guru database to select already existaing or planned CSP plants as representitve plants.
			  For France and Portugal no existing project matched the location with most potential. Hence the center of those NUTS2 regions where taken as location.
		* ts_csp.csv:
			* csp thermal generation data computed using parabolic trough model of oemof thermal module, with input data from pvgis irradiance data, extracted on 2023-03-30 with pvlib.
				* sources: 
					* https://oemof-thermal.readthedocs.io/en/latest/concentrating_solar_power.html (visited on 2023-04-05)
					* https://pvlib-python.readthedocs.io/en/stable/reference/generated/pvlib.iotools.get_pvgis_hourly.html (visited on 2023-04-05)
					* https://re.jrc.ec.europa.eu/pvg_tools/en/ (visited on 2023-04-05)
			    * csp-guru-2022-07-01.02:
		    * database of the existing csp plants
		    * source: 10.5281/zenodo.7112761
	* ENSPRESO
		* data for wind, solar and biomass potential in EU
		* source: https://doi.org/10.1016/j.esr.2019.100379
	* gitignored: ignored by git (for big files)
		* opsd-weather_data-2020-09-16
			* time series of country aggregated weather data from open power system data (temperature, DNI*cos(theta) and DHI)
			* source: https://doi.org/10.25832/weather_data/2020-09-16
	