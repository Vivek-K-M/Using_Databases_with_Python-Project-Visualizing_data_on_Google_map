-> Using the Google Places API with a Database and
Visualizing Data on Google Map

-> In this project, we are using the Google geocoding API
to clean up some user-entered geographic locations of
university names and then placing the data on a Google
Map.

Run the geoload.py program.   This program will read the input
lines in where.data and for each line check to see if it is already
in the database and if we don't have the data for the location,
call the geocoding API to retrieve the data and store it in
the database.


The geoload.py can be stopped at any time, and there is a counter
that you can use to limit the number of calls to the geocoding
API for each run.

Once you have some data loaded into geodata.sqlite, you can
visualize the data using the (geodump.py) program.  This
program reads the database and writes tile file (where.js)
with the location, latitude, and longitude in the form of
executable JavaScript code.

The file (where.html) consists of HTML and JavaScript to visualize
a Google Map.  It reads the most recent data in where.js to get
the data to be visualized.  Here is the format of the where.js file:

This is a JavaScript list of lists.  The syntax for JavaScript
list constants is very similar to Python so the syntax should
be familiar to you.

Simply open where.html in a browser to see the locations.  You
can hover over each map pin to find the location that the
gecoding API returned for the user-entered input.  If you
cannot see any data when you open the where.html file, you might
want to check the JavaScript or developer console for your browser.
