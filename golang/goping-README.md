# GoPing

Minimalistic webserver to handle and display time series of servers response
times.

## Technologies

 - Webserver is written in Go
 - Time Series Database (TSDB) is InfluxDB
 - Webview uses JQuery, Bootstrap and Chart.js

## API

### POST /api/1/pings

Adds new data (using JSON format, see `json/pings.json`).

### GET /api/1/pings/:origin/hours

Retrieves the transfer time averages (in ms) of `origin`, aggregated by hours.
It only returns data from the first recorded day.

### GET /

![Webview screenshot](./misc/screenshot.png)

Renders transfer time averages of one day, aggregated by hours, using a line
chart. From there, you can:

 - choose a different `origin` via the dropdown menu;
 - show the previous day;
 - show the next day;
 - go back to the first recorded day;
 - go to the current day.

## Installation and configuration

### Install and configure InfluxDB

InfluxDB is the TSDB that runs GoPing. To install it, please refer to the
[official documentation](https://influxdb.com/docs/v0.9/introduction/installation.html),
or if you prefer, you could just run a Docker container by using:

```
docker run -d -p 8083:8083 -p 8086:8086 tutum/influxdb
```

In any case, you need to have http://localhost:8086 serving the InfluxDB REST
API. You can now create the main database:

```
# Using curl
curl -G 'http://localhost:8086/query' --data-urlencode "q=CREATE DATABASE goping"

# Using HTTPie
http http://localhost:8086/query q=="CREATE DATABASE goping"
```

### Install and run GoPing

```
make install
$GOPATH/bin/goping
```

### Populate InfluxDB

By starting GoPing, you can now reach the webview at http://localhost:8080.
However, InfluxDB being empty, you'll first have to populate it with sample
datapoints. For instance, you can use the JSON file available at
`json/pings.json`. To do so, run:

```
# Using curl
curl -X POST -H "Content-Type: application/json" \
       localhost:8080/api/1/pings --data @json/pings.json

# Using HTTPie
http POST http://localhost:8080/api/1/pings < json/pings.json
```

## Documentation

To generate the documentation, just run `make doc`. It will start a local
webserver listening on port 6060. The documentation of the project should be
available at http://localhost:6060/pkg/github.com/aseure/goping.
