# Ecoforest API Specification

EcoForest is a Spanish Company focused on *"develop innovative products that were both economic and environmentally-friendly, with the intention of making the world a better place"* [1](https://ecoforest.es/en/more/about-us) They produce pellet stoves among other heater systems.

Their newer stoves include a remote control system based on a web page which design, usefulness and quality may be discussed. Moreover, some issues with the heater resistence not solved by the technical support push me to understand better how it works and to analyze if it can be controlled using a different system.

The web server is based on [thttpd/2.25b 29dec2003](http://www.acme.com/software/thttpd/) and the logic controlling the stove is based on a CGI that receives parameters over POST and returns the results. All requests have a common pattern based on a parameter that defines de operation id number and may include extra parameters required.

The base URL is:

- https://{{Server IP}}:8000/recepcion_datos_4.cgi

It requires basic authentication where the username is the Serial ID of the stove and the password is the first 8 digits of the password included in the user manual sticker.

## Repository Contents

This repository includes a Postman Collection with 53 requests that controls the basic behaviour of *"Bolonia"* EcoForest air stove. The same web application is used for other devices like air-water stoves but I have not been able to test it.

## To Do

- Scheduling commands are not included.
