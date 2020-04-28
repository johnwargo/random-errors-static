---
  layout: post
  title: Ionic HTTP Failure Unknown Error
  tags: 
  categories: Ionic
  comments: true
---

I'm working on a simple Ionic app I built as an example to publish publicly; it's a simple weather app that uses the OpenWeather API to display current conditions and forecast. The app runs great in the browser, but when you execute it on an Android Device, when the app connects to the Weather API, it immediately returns the following error:

```text
Http failure response for http://api.openweathermap.org/data/2.5/weather?lat=35.1607883&lon=-80.8581167&units=imperial&APPID=MYAPPID: 0 Unknown Error
```

I scratched my head for longer than I care to admit, but then recognized the problem. In my app's config file, I had the Weather API endpoint configured using HTTP. As soon as I switched it to HTTPS, the error went away and the app started working fabulously.

Apparently Android no longer likes non-secure endpoints for HTTP calls. 