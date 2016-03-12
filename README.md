:umbrella: weather-data :umbrella:
==========================================


This data stream acquired using the
[The Dark Sky Forecast API](https://developer.forecast.io/)
polls the API every minute to grab the distance of the nearest storm to Columbia University (rel. to [Butler Library](https://en.wikipedia.org/wiki/Butler_Library))  and stores that in a redis store. At the same time,
on every entry on the redis store, we calculate a moving average of the
air pressure and we send an alert via twitter, alerting us of the chance
of rain.


### Usage (TBD)

1. clone and get up in that folder
2. `websocketd --port=8080 --staticdir=. python monitor-soundcloud.py`
3. open a new terminal tab and run: `python -m SimpleHTTPServer`
4. open Chrome and navigate to: `localhost:8000`
5. Bask in the beauty of the data stream.