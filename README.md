# specmatch-apf-emp
Summer 2021 BSRC Breakthrough Listen project (A Search for Laser Technosignatures using APF Spectra).

   High-resolution spectroscopy has been used to detect the first extrasolar planets around sun-like stars, and to measure the masses of some of the thousands of planets detected via photometry. Current and next-generation spectrographs have the resolution necessary to go even further and detect components of exoplanet atmospheres as well as laser emission from modestly powered extraterrestrial lasers. One of the primary false positive scenarios for the laser line search, aside from cosmic rays, is telluric line contamination of stellar spectra. As starlight passes through the atmosphere, reflected light from the moon can illuminate the night sky, and leave an imprint on the stellar spectrum. Additionally, the night sky naturally emits and absorbs at specific wavelengths corresponding to the constituents of our own atmosphere. There are theoretical studies that attempt to predict the night sky emission, and with the Automated Planet Finder, we have an empirical measure of the night sky lines that we can compare to these models. By identifying all stellar features and telluric features, we can get closer to zeroing in on candidate laser lines. Auxiliary science in this project includes surveying interstellar absorption/emission features such as sodium.
    
   One of the goals of my project was to create a telluric line catalog of different stars and compare them to predicted theoretical telluric lines. At first I had to know how to deblaze and normalize spectra. I used tutorials from Haynes Stephens and Zoe Ko to write up my own tutorial on normalizing APF spectra. In order to correct for telluric contamination, I was going to use a Python code called TelFit, which was written to model and fit the telluric absorption spectrum into astronomical data. However, my mentor  Howard and I had trouble trying to install TelFit onto the data center so that we can record the data were going to obtain. Instead we used Keck and APF data to look for  sodium-D absorption features. The absorption features are located at specific orders of the data and I had to find out which order they showed up in. I zeroed in on the specifc wavelengths that sodium-D showed up in I was able to find the order they were in: order 11. After finding the order, I got a graph showing the raw Keck spectrum that includes the sodium-D lines. From there I deblazed and normalized the spectra by using Haynes Stevens's and Zoe Ko's tutorials.
   
   Next, I plotted the raw APF spectrum that includes the area of the sodium-D lines. I identified them and then asked Howard for the Keck specturm data to plot the raw Keck spectrum that included sodium-D lines. In order to interpolate, or plot over the normalized Keck  spectrum onto the normalized APF spectrum, I needed to plot both the raw APF and Keck spectrum data onto the same graph. That way I can find the overlap between the APF and Keck data. From there I created a new wavelength and flux array that consisted of the overlapping data and plotted those as well. Once I plotted the graph, I then intepolated the new flux array from Keck over the APF wavelength solution to compare the position of the sodium-D lines between the two plots and they lined up for the most part, however they differed by a few angstroms.    
