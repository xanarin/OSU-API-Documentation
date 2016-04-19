# Image API Specification

## API Endpoint
The API endpoint as of April 19, 2016 is https://content.osu.edu/v2/ohio/

## Retrieving All Images

#### Query
List of all approved images can be requested by appending the word 'images' to the endpoint. For example:
```
https://content.osu.edu/v2/ohio/images
```

#### Sample Response
_Ellipses mark possible repetition_
```json
{
    "data": {
        "images": [
            {
                "author": "Gabriela Avila",
                "description": "April 16, 2016 at the Global Star Party held at the Ohio State Planetarium.",
                "id": 55806,
                "link": "https://s3.amazonaws.com/ohiotd/images/000/055/806/featured/_MG_2840.jpg?1460858935",
                "publishedDate": "2016-04-19T11:50:42.253Z",
                "title": "Rooftop of Smith Lab at Sunset"
            },
            {
                "author": "Kristen Schoeff",
                "description": "Spring game O-H-I-O while checking out the OSUMB's practice field.",
                "id": 55808,
                "link": "https://s3.amazonaws.com/ohiotd/images/000/055/808/featured/Spring_Game_2016_OHIO.jpg?1460984242",
                "publishedDate": "2016-04-19T11:49:51.858Z",
                "title": "Future TBDBITL'ers"
            },
            {
                "author": "Rebecca Kemper",
                "description": "Urban Affairs Association (UAA) 2016 Conference San Diego, California",
                "id": 55736,
                "link": "https://s3.amazonaws.com/ohiotd/images/000/055/736/featured/image.jpeg?1458364931",
                "publishedDate": "2016-03-21T17:29:56.626Z",
                "title": "City & Regional Planning Researchers /  Alumni "
            },
            ...
        ]
    },
    "lastModified": "2016-04-19T12:00:15.890Z",
    "status": "success"
}
```

## Retrieving Images of the day

#### Query
List of all images of the day can be requested by querying the endpoint:
```
https://content.osu.edu/v2/image-of-the-day/images
```

#### Sample Response
_Ellipses mark possible repetition_
```json
{
    "data": {
        "images": [
            {
                "author": "",
                "id": 1215944,
                "link": "https://s3.amazonaws.com/ohiotd/images/000/055/801/featured/blob?1460748009",
                "publishedDate": "2016-04-18T20:00:00.000Z",
                "title": "Look up"
            },
            {
                "author": "",
                "id": 1214047,
                "link": "https://s3.amazonaws.com/ohiotd/images/000/055/713/featured/blob?1457655908",
                "publishedDate": "2016-04-17T20:00:00.000Z",
                "title": "The Greatest Place on Earth"
            },
            {
                "author": "",
                "id": 1212095,
                "link": "https://s3.amazonaws.com/ohiotd/images/000/055/723/featured/blob?1458091074",
                "publishedDate": "2016-04-16T20:00:00.000Z",
                "title": "An early spring sign on campus"
            }, ...
        ]
    },
    "lastModified": "2016-04-19T01:00:31.432Z",
    "status": "success"
}
_ Note: All linked images are actually in the JPEG format, even though that is not specified in the URL _
