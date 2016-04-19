# Garage API Specification

## API Endpoint
The API endpoint as of April 19, 2016 is https://content.osu.edu/v2/parking/garages/

## Retrieving garage information

#### Query
Information about all garages can be requested by appending the word 'availability' to the endpoint. For example:
```
https://content.osu.edu/v2/parking/garages/availability
```

#### Sample Response
_Ellipses mark possible repetition_
```json
{
    "data": {
        "garages": [
            {
                "capacity": 644,
                "count": 267,
                "currentAccess": [
                    "keycard",
                    "visitor"
                ],
                "lastUpdated": "2016-04-19T21:35:34.000Z",
                "link": "http://www.campusparc.com/osu/garages/11th-avenue",
                "name": "11th Avenue",
                "osuBuildingNumber": "352",
                "percentage": 41
            },
            {
                "capacity": 284,
                "count": 41,
                "currentAccess": [
                    "keycard",
                    "visitor"
                ],
                "lastUpdated": "2016-04-19T21:35:34.000Z",
                "link": "http://www.campusparc.com/osu/garages/west-lane",
                "name": "West Lane Avenue",
                "osuBuildingNumber": "892",
                "percentage": 14
            },
            ...
        ],
        "itemHash": "406067b15e20c172d73aae974dd20e78"
    },
    "lastModified": "2016-04-19T21:37:09.375Z",
    "status": "success"
}
```
