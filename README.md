# THIS IS AN AWFUL FORK, I'M JUST DOING IT SO I CAN C&P THE RESULT INTO DREAMHOST AND USE GITHUB TO EDIT. I'M AVOIDING THE TZ LOOKUP, SKIPPING HAVING A GOOGLE MAPS KEY

# sunrise
Display sunset and sunrise times as all day events from an iCalendar feed in Google Calendar, your phone or elsewhere.

## usage

Example calendar URL:

	http://sun.is.permanent.ee/?latitude=59.4388618469&longitude=24.7544727325&title=sunrise,sunset,length_civil&label_length_civil=☼&label_sunrise=↑&label_sunset=↓&start=-100&end=365&filename=sunrise.ics

Modify the parameters in the URL according to your needs. You will atleast need to modify latitude and longitude.

Add the above url into your Google Calendar at Other Calendars -> down arrow box thingie -> Add by URL

### latitude
The latitude of your location, in degrees.

	latitude=59.4388618469

### longitude
The longitude of your location, in degrees.

	longitude=24.7544727325

### title
This sets what the calendar events title will be. You can use any of the below variables in any order:

variable						| description
:---------------				| :---------
astronomical_twilight_begin		| Start of astronomical twilight
nautical_twilight_begin			| Start of nautical twilight
civil_twilight_begin			| Start of civil twilight
sunrise							| Sunrise
transit							| Noon
sunset							| Sunset
civil_twilight_end				| End of civil twilight
nautical_twilight_end			| End of nautical twilight
astronomical_twilight_end		| End of astronomical twilight
length							| Day length from Sunrise until Sunset
length_civil					| Day length for civil twilight
length_nautical					| Day length for nautical twilight
length_astronomical				| Day length for astronomical twilight

	title=sunrise,sunset,length,length_civil

### labels
Normally the values of the variables in the calendar event titles are not prefixed with any text to conserve space, but you can change that by adding an URL parameter with the variable name prefixed with 'label_'.

	label_astronomical_twilight_end=End%20of%20twilight

### start
What day to start the calendar on from today. 

	start=-100

### end
What day to end the calendar on from today.

	end=365

### filename
This is the filename of the file offered for download when you access the calendar URL directly. This needs to be the last URL parameter, because otherwise Google Calendar will not read anything from this URL and will silently fail.

	filename=sunrise.ics
