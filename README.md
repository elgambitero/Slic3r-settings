#elgambitero's Slic3r settings

##Introduction
Welcome to my personal Slic3r settings repo. This will hold the settings I rely on when I work with 3D printers, either at home or at work, and how I got to calibrate them.

[Slic3r][Slic3r] is a build code (gcode) generator for 3D printers. It is Open Source, gives access to a huge amount of parameters, and it's been around for enough time for it to be a reliable program. The GUI is not as pretty as [Cura][Cura], but that won't be a decisive parameter here.


It will be focusing on bq first pieces of equipment first (this is, [bq Hephestos][Hephestos] and 1st gen bq Witbox), by I may later add settings for my homemade prusa i2 SHODAN. (These are the printers I have access to for now.)
When it comes to materials, it will begin by including the parameters of bq PLA coils, and then will expand to other plastics as I acquire them.

##Criteria

These settings are configured following my near-OCD criteria when it comes to judge the quality of 3D prints, regardless of whether these are achievable or not with the Slic3r software, I'm keen on pursing them:

* **Layers must be even.**
	* On a vertical wall, every filament must be placed JUST on top of the previous one, and look the same as the previous one.
* **Even filament flow.**
	* No bubbles, no blobs, no random thinness, no nothing. STRAIGHT AND EVEN LINE.
	* That's why for each filament, in each colour, there will be a config file.
* **What is intended to fit in the CAD, MUST FIT in the real world.**
	* Including but not limited to bolts, grooves, pockets, drills.
	* The dimensions of the final part must have the same measures as in the CAD.
	* I don't buy arguments claiming that "those are just 3D printing tolerances" when some of the current 3D printers are equipped with heavy-duty linear systems. Tolerances can be narrowed thinner that just the nozzle diameter.
* **Support material must be something you can count on, without ruining the part's finish.**
	* I want complete geometric freedom, and for that you end up needing supports.
	* This one is difficult because the 3D printing community is still figuring out the best ways of generating toolpaths that build a properly tearable piece of support.
	* If I get my hands on a dual printer, this point will get more interesting
* **We are not in a hurry**
	* That's it, you can expect pretty slow build codes. I prefer waiting 72 hours for my part to print, that waiting a month for someone to mill it. Now that printers got that robust, taking days to print something big is not a big deal.
	* Don't worry about that previous clarification, small parts will still take about 20 minutes to print. This settings will be slow, but not THAT slow.
	* **LOW ACCELERATIONS!!!** Printers need low accelerations! With the GRBL gcode planner running in almost every 3D printer on the planet, I wonder why such high numbers like 5000 mm/s2 are that frequent. That barely takes the advantages of having accelerations (such as less mechanical stress, and more precision when tracing). A value of 200 mm/s2 is going to be hardcoded in every printer in this repo.

##Further reading

* The wiki of this repo will have further explanations about the methods used to calibrate each concerning aspect of 3D printing.
* [RichRap][RichRap] has been using and defending Slic3r from almost the very beggining, and has great documentation about 3D printing temperatures and the finish that comes with them. Reading his articles and following him is highly recommended.
	* [Slic3r is Nicer 1: Main settings and extruder calibration][Slic3rNicer1]
	* [Slic3r is Nicer 2: Filament and printing][Slic3rNicer2]
	* [Slic3r is Nicer 3: How low can you go?][Slic3rNicer3]



##Special thanks

* To [Adrian Bowyer][AdriBow], for the [RepRap project][RepRap].
* To [Alessandro Ranellucci][Aleran], author of [Slic3r][Slic3r]
* To [RichRap][RichRap], for sharing his knowledge about Slic3r usage


##License

Although this is not quite content creation, everything you can find here is licensed under Creative Commons 4.0 Attribution-ShareAlike  
<img src="./img/cc-by-sa.png" width="200" align="center">


[Aleran]: https://twitter.com/alranel
[AdriBow]: https://twitter.com/adrianbowyer
[RichRap]: http://richrap.blogspot.com
[Slic3rNicer1]: http://richrap.blogspot.com.es/2012/01/slic3r-is-nicer-part-1-settings-and.html
[Slic3rNicer2]: http://richrap.blogspot.com.es/2012/01/slic3r-is-nicer-part-2-filament-and.html
[Slic3rNicer3]: http://richrap.blogspot.com.es/2012/01/slic3r-is-nicer-part-3-how-low-can-you.html
[Slic3r]: http://slic3r.org
[Cura]: https://ultimaker.com/en/products/cura-software
[Hephestos]: http://www.bq.com/gb/prusa
[RepRap]: http://reprap.org
