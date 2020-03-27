# Coronavirus-Heroku-tracker (API) Version 0.1.1

## :warning: Remove Recovered Cases :warning:

[2019 Novel Coronavirus (nCoV) Data Repository, provided
by JHU CCSE](https://github.com/CSSEGISandData/2019-nCoV) removed the support of recovered cases. The /recovered endpoint was removed !


All requests must be made to the base url: ``https://covid192.herokuapp.com/``. You can try it out in your browser to further inspect responses.

Getting confirmed cases, deaths, and recoveries:

```http
GET /
```
```json
{ "latest": { ... }, "confirmed": { ... }, "deaths": { ... } }
```

Getting just confirmed:

```http
GET /confirmed
```
```json
{ "latest": 418678, "locations": [ ... ] }
```

Getting just deaths:

```http
GET /deaths
```
```json
{ "latest": 18625, "locations": [ ... ] }
```

Getting just latest data:

```http
GET /latest
```
```json
{ "confirmed": 418678, "deaths": 18625 }
```

## Prerequisites

You will need the following things properly installed on your computer.

* [Python 3](https://www.python.org/downloads/) (with pip)
* [Flask](https://pypi.org/project/Flask/)
* [Heroku](https://devcenter.heroku.com/articles/heroku-cli)

## Installation

* `git clone https://github.com/hasancafarov/Covid-19-best-API`
* `cd Covid-19-Api`
* `pip install -r requirements.txt`

## Running / Development

* `python app.py`
* Visit your app at [http://localhost:5000](http://localhost:5000).

### Deploying

* Create a Heroku account
* Create a Heroku application
* `heroku login`
* `git init`
* `heroku git:remote -a <AppName>`
* `git add .`
* `git commit -am "first commit"`
* `git push heroku master`

### Testing

* Visit your application webpage
* `https://<AppName>.herokuapp.com/`

## License

The data is available to the public strictly for educational and academic research purposes.
