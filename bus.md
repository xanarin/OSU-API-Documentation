# Bus API Specification for CABS busses

## API Endpoint
The API endpoint as of April 19, 2016 is https://content.osu.edu/v2/bus/routes/

## Bus Lines
Each bus line has a particular code, as specified below:
- Medical Center - MC
- Campus Loop North - CLN
- Buckeye Village - BV
- Campus Loop South - CLS
- East Residential - ER
- North Express - NE

## Retrieving stop information

#### Query
Information about all stops for a given line is given by appending the line code to the endpoint. For example:
```
https://content.osu.edu/v2/bus/routes/CLN
```
gives all information about stops on the CLN route.

#### Sample Response
_Ellipses mark possible repetition_
```json
{
    "data": {
        "patterns": [
            {
                "direction": "Circular",
                "encodedPolyline": "a}csFtkyyN?KE{@KiAK{@K_@Px@JdAHdA@jA?f@CrAChAAv@Ad@A`@?N@HBFDBJ@x@D~AJ|DJJCJIFKBS@WVmO?OAKCKEGKCYAcACkBC}@Em@?q@Fk@LMAMQI]Oe@e@oA_@{@Qc@Qg@KYESG[Ea@C]A[?S?c@?_@?o@Am@Am@?}@KsBe@wC{@wDcAeF]}AWmAMmAGcBXgKv@ab@R}Z",
                "id": "314",
                "length": 9077
            },
            {
                "direction": "Circular",
                "encodedPolyline": "i_csFdysyNVCn@INCH?FDDH@N?R?rAFrAF|@Fr@L`BFnA@j@Kt@OdAIl@En@C`A@|AD`ADb@FRHJJDbAKbAOvBQl@Q^AhFo@`BQJ?FJ?dBGbH?|AAhA@ZHFJ@~ADL@LJDLBXAd@AnA@f@Bh@Fb@L|@T~ARdB@p@?j@A^CPGHsAb@w@PaCD_BBc@A{@@}@@aAJe@Di@H[Ha@NsAf@wAh@qBp@_C\\{BNaD@eBMmCg@mB_@o@SsAg@aA[iB[[GMEIKIOCOAS?]@{A?U?QESIQIKGGKGOCgBKe@EEBEFCJ?PArAC|ABMMnHI|EEvBErBCxAIpB?vBEnBAt@An@EzAAp@Al@@f@Bh@@\\Db@Hl@Nv@h@fCt@lDj@nC^dBLbAHfAB|A@fA@jA?r@?n@?l@@ZHl@Hf@HZPh@Pd@Pb@LVN^LZRh@Pr@Nx@Hh@Dj@Bh@@j@",
                "id": "429",
                "length": 15160
            },
            ...
        ],
        "stops": [
            {
                "id": "10",
                "latitude": 40.002248658569,
                "longitude": -83.038192391396,
                "name": "BEVIS HALL"
            },
            {
                "id": "11",
                "latitude": 40.002302078763,
                "longitude": -83.039825856686,
                "name": "CARMACK CORNER"
            },
            ...
        ]
    },
    "lastModified": "2016-04-19T21:24:00.555Z",
    "status": "success"
}
```


## Retrieving vehicle information

#### Query
Information about all busses on a given line is given by appending the line code and the string '/vehicles' to the endpoint. For example:
```
https://content.osu.edu/v2/bus/routes/CLN/vehicles
```
gives all information about busses on the CLN route.

#### Sample Response
```json
{
    "data": {
        "vehicles": [
            {
                "delayed": false,
                "destination": "NORTH CAMPUS",
                "distance": 5029,
                "heading": 67,
                "id": "1105",
                "latitude": 40.00395209102307,
                "longitude": -83.03058171676378,
                "patternId": "314",
                "routeCode": "CLN",
                "speed": 51,
                "updated": "2016-04-19T21:27:28.000Z"
            },
            {
                "delayed": false,
                "destination": "WEST CAMPUS",
                "distance": 2100,
                "heading": 170,
                "id": "1102",
                "latitude": 39.99607742041872,
                "longitude": -83.01480182848479,
                "patternId": "429",
                "routeCode": "CLN",
                "speed": 25,
                "updated": "2016-04-19T21:27:09.000Z"
            },
            {
                "delayed": false,
                "destination": "SOUTH CAMPUS",
                "distance": 1862,
                "heading": 172,
                "id": "1103",
                "latitude": 40.002720749169065,
                "longitude": -83.0107431244432,
                "patternId": "430",
                "routeCode": "CLN",
                "speed": 10,
                "updated": "2016-04-19T21:27:22.000Z"
            }
        ]
    },
    "lastModified": "2016-04-19T21:27:30.705Z",
    "status": "success"
}
```

## Retrieving basic line information

#### Query
Information about all lines is given by querying the endpoint. For example:
```
https://content.osu.edu/v2/bus/routes
```

#### Sample Response
```json
{
    "data": {
        "routes": [
            {
                "code": "BV",
                "color": "#006600",
                "name": "BUCKEYE VILLAGE"
            },
            {
                "code": "CLS",
                "color": "#cc0000",
                "name": "CAMPUS LOOP SOUTH"
            },
            {
                "code": "ER",
                "color": "#0033cc",
                "name": "EAST RESIDENTIAL"
            },
            {
                "code": "MC",
                "color": "#ff66cc",
                "name": "MEDICAL CENTER "
            },
            {
                "code": "CLN",
                "color": "#999999",
                "name": "CAMPUS LOOP NORTH"
            },
            {
                "code": "NE",
                "color": "#ff6600",
                "name": "NORTH EXPRESS"
            }
        ]
    },
    "lastModified": "2016-04-15T05:04:00.373Z",
    "status": "success"
}
```
