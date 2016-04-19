# OSU API Reference

## Purpose
This reference is intended to be used for developers who would like to access the OSU APIs for information such as:
- Bus Arrival Times and Current Locations
- Locations of all dining halls, their menus, and all nutritional information
- Garage locations and their current statuses
- OSU's Image Of the Day
- Class searches (replaced course catalog university-wide in 2016)

These APIs should be much more dependable than programmatically scraping OSU's public-facing websites or tracking values by hand.

## Collection Methodology
All of the APIs listed here are used by the official Ohio State University iOS App, "Ohio State". This app was used in conjunction with the HTTPS proxy capabilities of [Charles](charlesproxy.com) to discover and document all APIs.

## Actual Usage
All API endpoints as listed in this repository can be accessed using a secure HTTPS connection, and the **GET** HTTP verb.

## Disclaimer
I am not associated with the developers of the OSU App, and am not working with the backend services team to provide this API to the public. My goal for this project was to merely document the already-existing API and make it easier for students to get information about university services, and build better ways of analyzing and visualizing this data.
