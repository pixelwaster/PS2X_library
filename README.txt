  Super amazing PS2 controller Arduino Library v1.9.1
		details and example sketch: 
			http://www.billporter.info/?p=240

    Original code by Shutter on Arduino Forums

    Revamped, made into lib by and supporting continued development:
              Bill Porter
              www.billporter.info

	 Contributers:
		Eric Wetzel (thewetzel@gmail.com)
		Kurt Eckhardt

  Lib version history
    0.1 made into library, added analog stick support. 
    0.2 fixed config_gamepad miss-spelling
        added new functions:
          NewButtonState();
          NewButtonState(unsigned int);
          ButtonPressed(unsigned int);
          ButtonReleased(unsigned int);
        removed 'PS' from beginning of ever function
    1.0 found and fixed bug that wasn't configuring controller
        added ability to define pins
        added time checking to reconfigure controller if not polled enough
        Analog sticks and pressures all through 'ps2x.Analog()' function
        added:
          enableRumble();
          enablePressures();
    1.1  
        added some debug stuff for end user. Reports if no controller found
        added auto-increasing sentence delay to see if it helps compatibility.
    1.2
        found bad math by Shutter for original clock. Was running at 50kHz, not the required 500kHz. 
        fixed some of the debug reporting. 
	1.3 
	    Changed clock back to 50kHz. CuriousInventor says it's suppose to be 500kHz, but doesn't seem to work for everybody. 
	1.4
		Removed redundant functions.
		Fixed mode check to include two other possible modes the controller could be in.
       Added debug code enabled by compiler directives. See below to enable debug mode.
		Added button definitions for shapes as well as colors.
	1.41
		Some simple bug fixes
		Added Keywords.txt file
	1.5
		Added proper Guitar Hero compatibility
		Fixed issue with DEBUG mode, had to send serial at once instead of in bits
	1.6
		Changed config_gamepad() call to include rumble and pressures options
			This was to fix controllers that will only go into config mode once
			Old methods should still work for backwards compatibility 
    1.7
		Integrated Kurt's fixes for the interrupts messing with servo signals
		Reorganized directory so examples show up in Arduino IDE menu
    1.8
		Added Arduino 1.0 compatibility. 
    1.9
       Kurt - Added detection and recovery from dropping from analog mode, plus
       integrated Chipkit (pic32mx...) support
    1.9.1
       Modified avr clk and byte values. Changed private variable names to make
       reading easier (added current_ test_ to button button &c). 


