# python-web-flask-mvc-jaeger-prometheus-single-call

## Description
Three spans are called in a single
call. Creates a simple web page with
a single button. When the button is
clicked spans are created and opentracing
output is sent to the jaeger ui.

## STEP 1
Click on `Send trace` to create
data for jaeger ui to collect.

## STEP 2
Navigate to jaeger ui via nav bar
or http://localhost:16686. Look for
service named `py-service`.

## STEP 3
To check prometheus navigate to prometheus
dashboard via nav bar or http://localhost:9090.
- Goto Classic UI
  - Query for `scrape_duration_seconds`

## Tech stack
- python
  - flask
  - opentracing-api
  - opentracing-sdk
  - opentelemetry-exporter-jaeger

## Docker stack
- python:latest
- jaegertracing/all-in-one:1.17
- prom/prometheus

## To run
`sudo ./install.sh -u`
- Available http://localhost

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
[ Code concept ] (https://www.splunk.com/en_us/blog/devops/getting-started-with-opentelemetry-python-v1-0-0.html)
