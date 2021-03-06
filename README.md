Getting Started

Please run:

sudo pip install -r requirements.txt

then you can run the flask application:

flask run


#Welcome to the Science of Space 101.

The following document is a user's manual and an informative article about the website, how it works and what exactly it does. This website is made for amateur astronomers. Often when people engage in astronomy and for me, astrophotography, they have to figure where exactly the object or planet they want to look at is. There are trillions of stars in the night sky and parsing them is a uniquely difficult job. My goal with this project was to provide a mathematical and informative method of supporting the quest of fellow astronomers to find and locate objects in the night sky as well as provide a space for the user to upload their own astronomy pictures as well.

The website has 3 main components, picture upload and displaying area, a raw data download portal and lastly an orbit model and display that will allow the astronomer to locate the planet or star of their choice in the sky. The program itself draws data from NASA's databases and in particular JPL Horizons which is maintained by Harvard ABS, the International Astronomical Association and Caltech. It suffices to say that the information provided through these databases is more reliable and accurate than any apps that you may find on the web that do not display live data but rather models made by programmers that are not free. In contrast, the Science of Space is a free website that promises to produce more accurate information.

Using the orbit modeling engine: 

When you first open the website you will see a homepage that describes the site and a series of tabs in a navigation bar (that is mobile-friendly) at the top of the page. In order to model the object that you are interested in, you must insert the correct spelling, capitalization, and format because the database has all sorts of objects and if you spell something wrong you will most likely end up querying for the wrong object. For common objects such as planets with orbiting bodies that are well known to the public sphere, you must put in a numeric query into the portal. What this means is that if you want to look up Mars then you must input 499. Now you may be wondering how you are going to know what the number for the astronomical object is, whether you have to use the number for the object you are interested in, or why you have to do this in the first place. The reason why is easiest to answer. Lets us take Mars for example. The Horizons database stores any objects or missions associated with Mars on its database as well. Therefore, when JPL was creating the query module astropy, they figured that rather than having to figure out what object related to Mars a user is talking about, they could be pickier and ask for the IAU ID assigned to the object. Now, there are a couple of ways of figuring out this ID. The easiest is to search up on google JPL Horizons and enter in the object name, the number that appears to the right of the object name is the IAU ID. So if you were to go on to the web portal and put in the object name Mars, it may ask you what object you are talking about. In that case, you will have to select the object on JPL's site. That way you can find out the number.

Here are a couple ID's in case you do not want to look up the ID assigned 199 - Mercury, 299 - Venus, 399 - Earth, 499 - Mars, 599 - Jupiter, 699 - Saturn, 799 - Uranus, 899, - Neptune and so on. You could even click on the portal tab and in the query bar, you could enter a random number to see what you will get. There are over a million objects in the database and so you might get something "out of this world" :). There are also other objects that you could probably just search by name, Pluto for example or even Ceres which is a dwarf planet. If you input something incorrectly you will get a server error. Just click the back button and enter a legitimate query. You can even search for comets like C/2012 Q1 (kowalski) or even Halley’s comet.

Here is a link to a quick 40-sec youtube video that demonstrates this:

[a link](https://youtu.be/j7SDbqx_0j8)

Once you hit that query button you should see a super cool loading screen. The query is now being processed and the code is creating some orbital calculations and linear transformations. This may take a while due to the size and complexity of the data being processed and plotted. Once the screen loads, you will see a rotating globe with some green dots on it. That globe is a 3-dimensional representation of Earth and the green dots plot the annual path of the object that you queried superimposed on the atmosphere. That way you can see the optimal geolocation from where the object you queried can be viewed. For example, if you were to see green dots over Russia or Argentina then those would be optimal locations for viewing the object. Think of it in the same way that one would look at the best place from where to watch the solar eclipse.

The second plot generated is a graph of the object's movement in the sky and the y-axis is the elevation. The elevation tells you in degrees how far the object is above the white line or the horizon based on the location you are at when you query (specifically your IP address). The x-axis, in this case, is in degrees. The Earth moves 360* degrees in a day and so each degree is 1/360th of a day or 4 minutes to be precise. The red line demonstrates the current position of the object on the curve. So if the red line you are looking at intersects with the curve at 10* degrees elevation and 244* then the object you queried is exactly 10 degrees above the horizon and if you moved clockwise it would be 244 degrees from North. Below the diagram is the current location of the user and a paragraph explaining the data.

If you click on the data tab you will also be asked to submit a query for an astronomical object. You will need to follow the IAU guidelines to get a successful JSON query. I highly recommend you look at the paragraph on the portal if you have not already. Once the object is submitted you will see a loading screen and then a new screen will load. This screen will say raw data and there will be a link below. The link is a CSV file will all the raw data that I used to generate the plots in the query portal and it is generally useful for any telemetry measurements that amateur astronomers may want to make.

Then there is the uploads pictures tab. Here any user can upload their pictures by selecting files from their computer's local folders and then upload it to the website. This upload page will only pictures and all related picture formats. Lastly, after you submit you will be able to see your uploaded picture on the uploaded pictures page. The day you submitted your picture will also be displayed next to it. If the website managers like your picture it might be highlighted on a display tab like Jupiter, Saturn, and the Moon are now.

That is essentially the summary of the website usage, I hope this helped.
For additional Q&A please contact: Aakash Mishra scienceofspace101@gmail.com


