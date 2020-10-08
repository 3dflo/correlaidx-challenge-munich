# The datenguide chatbot

The [datenguide project](https://datengui.de/) creates an interface to the 
statistics provided by the local authorities in Germany. However, one still
needs programming knowledge to use the datenguide API and query the
statistics. In order to make the data more accessible to the general public,
we build a chatbot, which utilizes the datenguide API and specifically answers 
your questions and renders visualizations about diverse topics in Bavaria.

This project was created by the Munich local chapter of Correlaid for the 
CorrelaidX challenge.

![Chatbot](https://github.com/CorrelAid/correlaidx-challenge-munich/blob/master/.github/chatbot_pic3.PNG)

## Getting started

- Create a Python virtual environment, and install all dependencies as 
specified in `requirements.txt`.
- Navigate to the `/App` folder and run `python app.py`.
- Open `localhost:5000` in the browser to interact with the chatbot.
- Be sure to use either Chrome or Firefox as the browser to have the best
rending effects.
- If you are pip installing geopandas, make sure to install the dependencies. Maybe try
`pip install wheel
pip install pipwin
pipwin install numpy
pipwin install pandas
pipwin install shapely
pipwin install gdal
pipwin install fiona
pipwin install pyproj
pipwin install six
pipwin install rtree
pipwin install geopandas`. Otherwise,  download GDAL and fiona via https://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal and https://www.lfd.uci.edu/~gohlke/pythonlibs/#fiona or use conda.

## Dialog flow

The chatbot first asks the user for her favorite city in Bavaria and then
for a specific topic of interest. It then uses the datenguide API to search
the regional statistics database for data related to the given city and topic.
Finally it renders a plot using the appropriate data. The user can also
download the raw data of the plot in the csv format.

## Tech stack

The chatbot is built as a web application using the Flask framework. The 
SpaCy library is used to process the text input.