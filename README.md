# adhan-oman
a forked version of a [gist](https://gist.github.com/skeeph/3293106) that includes Oman adhan parameters. Please note the elevations of cities in Oman. 

Reference for Oman Prayer Times:

https://www.mara.gov.om/calendar_page2.asp

# Help and Manual

User's Manual:
http://praytimes.org/manual

Calculation Formulas:
http://praytimes.org/calculation


# API

	getTimes (date, coordinates, timeZone [, dst [, timeFormat]])

	setMethod (method)       // set calculation method
	adjust (parameters)      // adjust calculation parameters
	tune (offsets)           // tune times by given offsets

	getMethod ()             // get calculation method
	getSetting ()            // get current calculation parameters
	getOffsets ()            // get current time offsets

# Sample Usage
    from adhan import PrayTimes

    prayTimes = PrayTimes()
    prayTimes.setMethod('Oman')
    times = prayTimes.getTimes(date_of_interest, (23.58, 58.35, 26), 4) # note the elevation after the coordinates.

    for i in ['Fajr', 'Sunrise', 'Dhuhr', 'Asr', 'Maghrib', 'Isha']:
        print(i + ': ' + times[i.lower()])


# License and Copyright

praytimes.py: Prayer Times Calculator (ver 2.3)

Copyright (C) 2007-2011 PrayTimes.org

Python Code: Saleem Shafi, Hamid Zarrabi-Zadeh

Original js Code: Hamid Zarrabi-Zadeh

Python Code (Updated): Ali Kuddah

License: GNU LGPL v3.0

TERMS OF USE:
	Permission is granted to use this code, with or
	without modification, in any website or application
	provided that credit is given to the original work
	with a link back to PrayTimes.org.

This program is distributed in the hope that it will
be useful, but WITHOUT ANY WARRANTY.

PLEASE DO NOT REMOVE THIS COPYRIGHT BLOCK.

## From Python code original author 
From Khabib Murtuzaaliev(skeeph):
    I'm not author of this library, but I have found and corrected a few of errors in this code
   
