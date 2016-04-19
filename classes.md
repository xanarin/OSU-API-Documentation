# Class API Specification

## API Endpoint
The API endpoint as of April 19, 2016 is https://content.osu.edu/v2/classes/

## Searching for Classes

#### Query
Searches for classes can be requested by appending the word 'search', and specifying the search query as a URL-encoded parameter labeled as 'q'. For example:
```
https://content.osu.edu/v2/classes/search?q=Software
```
searches for all classes associated with the term "Software"

The app advertises that is possible to query classes using:
- Academic Program
- Building
- Campus
- Course Title
- Description
- Instructor
- Subject

#### Sample Response
_Ellipses mark possible repetition_
```json
{
    "data": {
        "activeFilters": [],
        "activeSort": "",
        "courses": [
            {
                "course": {
                    "academicCareer": "Graduate",
                    "academicGroup": "Engineering",
                    "academicOrg": "D1435",
                    "allowMultiEnroll": "N",
                    "campus": "Columbus",
                    "campusCode": "COL",
                    "catalogNumber": "5022",
                    "cipCode": "14.0901",
                    "component": "Lecture",
                    "courseAttributes": [],
                    "courseId": "155986",
                    "description": "Intellectual foundations of software engineering; design-by-contract principles; mathematical modeling of software functionality; component-based software from client perspective; layered data representation. Previous programming experience in any language required.\r\nPrereq: At least one term of Calculus. Not open to students with credit for 2221, 2231, 4221, 321, or 502. Not open to students enrolled in a CSE or CIS major.",
                    "effectiveDate": "2013-08-20",
                    "effectiveStatus": "A",
                    "equivalentId": "S1807",
                    "grading": "Graded",
                    "maxUnits": 3,
                    "minUnits": 3,
                    "offeringNumber": "3",
                    "primaryComponent": "LEC",
                    "repeatUnitsLimit": 3,
                    "shortDescription": "SW 1: Components",
                    "subject": "CSE",
                    "subjectDesc": "Computer Science & Engineering",
                    "term": "Spring 2016",
                    "title": "Software I: Software Components"
                },
                "sections": [
                    {
                        "_parent": "155986-3-1162",
                        "academicGroup": "ENG",
                        "academicOrg": "D1435",
                        "associatedClass": "10",
                        "attributes": [],
                        "autoEnrollSection1": "0011",
                        "autoEnrollSection2": null,
                        "autoEnrollWaitlist": true,
                        "campus": "Columbus",
                        "cancelDate": null,
                        "career": "GRAD",
                        "catalogNumber": "5022",
                        "classNumber": "9745",
                        "combinedSection": "Closed",
                        "component": "Lecture",
                        "consent": false,
                        "courseDescription": "Intellectual foundations of software engineering; design-by-contract principles; mathematical modeling of software functionality; component-based software from client perspective; layered data representation. Previous programming experience in any language required.\r\nPrereq: At least one term of Calculus. Not open to students with credit for 2221, 2231, 4221, 321, or 502. Not open to students enrolled in a CSE or CIS major.",
                        "courseId": "155986",
                        "courseOfferingNumber": 3,
                        "courseTitle": "Software I: Software Components",
                        "description": "SW 1: Components",
                        "endDate": "2016-04-25",
                        "enrollmentStatus": "Closed",
                        "enrollmentTotal": 2,
                        "equivalentCourseId": null,
                        "holidaySchedule": "OSUSIS",
                        "instructionMode": "In Person",
                        "location": "CS-COLMBUS",
                        "meetingDays": "",
                        "meetings": [
                            {
                                "buildingCode": "279",
                                "buildingDescription": "Dreese Lab 357",
                                "buildingDescriptionShort": "DL 357",
                                "endDate": "2016-04-25",
                                "endTime": "8:55 am",
                                "facilityCapacity": 45,
                                "facilityDescription": "Dreese Laboratories",
                                "facilityDescriptionShort": "Dreese Lab",
                                "facilityGroup": false,
                                "facilityId": "DL0357",
                                "facilityType": "1B",
                                "friday": false,
                                "instructors": [
                                    {
                                        "displayName": "Jeremy John Morris",
                                        "email": "morris.343@osu.edu",
                                        "role": "PI"
                                    }
                                ],
                                "meetingNumber": 1,
                                "monday": false,
                                "room": "357",
                                "saturday": false,
                                "standingMeetingPattern": null,
                                "startDate": "2016-01-11",
                                "startTime": "8:00 am",
                                "sunday": false,
                                "thursday": true,
                                "tuesday": true,
                                "wednesday": false
                            }
                        ],
                        "minimumEnrollment": 0,
                        "primaryInstructorSection": "0010",
                        "secAcademicGroup": "ENG",
                        "secCampus": "COL",
                        "secCatalogNumber": "5022",
                        "section": "0010",
                        "sessionCode": "1",
                        "sessionDescription": "Regular Academic Term",
                        "startDate": "2016-01-11",
                        "status": "A",
                        "subject": "CSE",
                        "subjectDesc": "Computer Science & Engineering",
                        "term": "Spring 2016",
                        "termCode": "1162",
                        "type": "E",
                        "waitlistCapacity": 999,
                        "waitlistTotal": 0
                    },...
                ]
            },
            {
                "course": {
                    "academicCareer": "Undergraduate",
                    "academicGroup": "Engineering",
                    "academicOrg": "D1435",
                    "allowMultiEnroll": "N",
                    "campus": "Columbus",
                    "campusCode": "COL",
                    "catalogNumber": "2221",
                    "cipCode": "14.0901",
                    "component": "Lecture",
                    "courseAttributes": [
                        {
                            "description": "NWK LMA MNS MRN Course Fee $50",
                            "name": "CRSF",
                            "value": "CFR50"
                        },
                        {
                            "description": "EM test administered by department of instruction",
                            "name": "EXAM",
                            "value": "DEPT"
                        }
                    ],
                    "courseId": "150505",
                    "description": "Intellectual foundations of software engineering; design-by-contract principles; mathematical modeling of software functionality; component-based software from client perspective; layered data representation.\r\nPrereq: 1211 (203) or 1212 or 1221 (205) or 1222 (202) or 1223 (201) or 204 or EnGraph 167 or Engr 1221, or 1281.01H, or 1281.02H, or CSE Placement Level A. Concur: Math 1151 or 1161.01 or 1161.02. Not open to students with credit for 4221, 321, 502, or 5022. This course is available for EM credit.",
                    "effectiveDate": "2016-01-10",
                    "effectiveStatus": "A",
                    "equivalentId": {},
                    "grading": "Graded",
                    "maxUnits": 4,
                    "minUnits": 4,
                    "offeringNumber": "1",
                    "primaryComponent": "LEC",
                    "repeatUnitsLimit": 4,
                    "shortDescription": "SW 1: Components",
                    "subject": "CSE",
                    "subjectDesc": "Computer Science & Engineering",
                    "term": "Summer 2016",
                    "title": "Software I: Software Components"
                },
                "sections": [
                    {
                        "_parent": "150505-1-1164",
                        "academicGroup": "ENG",
                        "academicOrg": "D1435",
                        "associatedClass": "10",
                        "attributes": [
                            {
                                "description": "NWK LMA MNS MRN Course Fee $50",
                                "name": "CRSF",
                                "value": "CFR50"
                            },
                            {
                                "description": "EM test administered by department of instruction",
                                "name": "EXAM",
                                "value": "DEPT"
                            }
                        ],
                        "autoEnrollSection1": "0011",
                        "autoEnrollSection2": null,
                        "autoEnrollWaitlist": true,
                        "campus": "Columbus",
                        "cancelDate": null,
                        "career": "UGRD",
                        "catalogNumber": "2221",
                        "classNumber": "1242",
                        "combinedSection": "Closed",
                        "component": "Lecture",
                        "consent": false,
                        "courseDescription": "Intellectual foundations of software engineering; design-by-contract principles; mathematical modeling of software functionality; component-based software from client perspective; layered data representation.\r\nPrereq: 1211 (203) or 1212 or 1221 (205) or 1222 (202) or 1223 (201) or 204 or EnGraph 167 or Engr 1221, or 1281.01H, or 1281.02H, or CSE Placement Level A. Concur: Math 1151 or 1161.01 or 1161.02. Not open to students with credit for 4221, 321, 502, or 5022. This course is available for EM credit.",
                        "courseId": "150505",
                        "courseOfferingNumber": 1,
                        "courseTitle": "Software I: Software Components",
                        "description": "SW 1: Components",
                        "endDate": "2016-07-29",
                        "enrollmentStatus": "Open",
                        "enrollmentTotal": 38,
                        "equivalentCourseId": null,
                        "holidaySchedule": "OSUSIS",
                        "instructionMode": "In Person",
                        "location": "CS-COLMBUS",
                        "meetingDays": "",
                        "meetings": [
                            {
                                "buildingCode": "279",
                                "buildingDescription": "Dreese Lab 357",
                                "buildingDescriptionShort": "DL 357",
                                "endDate": "2016-07-29",
                                "endTime": "10:05 am",
                                "facilityCapacity": 45,
                                "facilityDescription": "Dreese Laboratories",
                                "facilityDescriptionShort": "Dreese Lab",
                                "facilityGroup": false,
                                "facilityId": "DL0357",
                                "facilityType": "1B",
                                "friday": true,
                                "instructors": [
                                    {
                                        "displayName": "Diego Sebastian Zaccai",
                                        "email": "zaccai.1@osu.edu",
                                        "role": "PI"
                                    }
                                ],
                                "meetingNumber": 1,
                                "monday": true,
                                "room": "357",
                                "saturday": false,
                                "standingMeetingPattern": null,
                                "startDate": "2016-05-11",
                                "startTime": "9:10 am",
                                "sunday": false,
                                "thursday": true,
                                "tuesday": true,
                                "wednesday": true
                            }
                        ],
                        "minimumEnrollment": 0,
                        "primaryInstructorSection": "0010",
                        "secAcademicGroup": "ENG",
                        "secCampus": "COL",
                        "secCatalogNumber": "2221",
                        "section": "0010",
                        "sessionCode": "1S",
                        "sessionDescription": "Summer Term",
                        "startDate": "2016-05-11",
                        "status": "A",
                        "subject": "CSE",
                        "subjectDesc": "Computer Science & Engineering",
                        "term": "Summer 2016",
                        "termCode": "1164",
                        "type": "E",
                        "waitlistCapacity": 999,
                        "waitlistTotal": 1
                    }, ...
                ]
            }, ...
          ]
          "currentItemCount": 200,
          "filters": [
              {
                  "items": [
                      {
                          "count": 188,
                          "link": "?q=Software&p=1&term=1162",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "1162",
                          "title": "Spring 2016"
                      },
                      {
                          "count": 37,
                          "link": "?q=Software&p=1&term=1164",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "1164",
                          "title": "Summer 2016"
                      },
                      {
                          "count": 218,
                          "link": "?q=Software&p=1&term=1168",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "1168",
                          "title": "Autumn 2016"
                      }
                  ],
                  "slug": "term",
                  "title": "Term"
              },
              {
                  "items": [
                      {
                          "count": 410,
                          "link": "?q=Software&p=1&campus=COL",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "COL",
                          "title": "Columbus"
                      },
                      {
                          "count": 7,
                          "link": "?q=Software&p=1&campus=LMA",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "LMA",
                          "title": "Lima"
                      },...
                  ],
                  "slug": "campus",
                  "title": "Campus"
              },
              {
                  "items": [
                      {
                          "count": 213,
                          "link": "?q=Software&p=1&subject=CSE",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "CSE",
                          "title": "Computer Science & Engineering"
                      },
                      {
                          "count": 45,
                          "link": "?q=Software&p=1&subject=BUSMGT",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "BUSMGT",
                          "title": "Business Admin: Management Sci"
                      }, ...
                  ],
                  "slug": "subject",
                  "title": "Subject"
              },
              {
                  "items": [
                      {
                          "count": 0,
                          "link": "?q=Software&p=1&academic-career=DENT",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "DENT",
                          "title": "Dentistry"
                      },
                      {
                          "count": 114,
                          "link": "?q=Software&p=1&academic-career=GRAD",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "GRAD",
                          "title": "Graduate"
                      }, ...
                  ],
                  "slug": "academic-career",
                  "title": "Academic Career"
              },
              {
                  "items": [
                      {
                          "count": 24,
                          "link": "?q=Software&p=1&academic-program=AGR",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "AGR",
                          "title": "Food, Agric & Environ Science"
                      },
                      {
                          "count": 68,
                          "link": "?q=Software&p=1&academic-program=ASC",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "ASC",
                          "title": "Arts and Sciences"
                      }, ...
                  ],
                  "slug": "academic-program",
                  "title": "Academic Program"
              },
              {
                  "items": [
                      {
                          "count": 0,
                          "link": "?q=Software&p=1&component=CLN",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "CLN",
                          "title": "Clinical"
                      },
                      {
                          "count": 0,
                          "link": "?q=Software&p=1&component=FLD",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "FLD",
                          "title": "Field Experience"
                      }, ...
                  ],
                  "slug": "component",
                  "title": "Component"
              },
              {
                  "items": [
                      {
                          "count": 54,
                          "link": "?q=Software&p=1&class-attribute=EM%20test%20administered%20by%20department%20of%20instruction",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "EM test administered by department of instruction",
                          "title": "EM test administered by department of instruction"
                      },
                      {
                          "count": 48,
                          "link": "?q=Software&p=1&class-attribute=NWK%20LMA%20MNS%20MRN%20Course%20Fee%20%2450",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "NWK LMA MNS MRN Course Fee $50",
                          "title": "NWK LMA MNS MRN Course Fee $50"
                      }, ...
                  ],
                  "slug": "class-attribute",
                  "title": "Class Attribute"
              },
              {
                  "items": [
                      {
                          "count": 84,
                          "link": "?q=Software&p=1&catalog-number=1xxx",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "1xxx",
                          "title": "1xxx"
                      },
                      {
                          "count": 142,
                          "link": "?q=Software&p=1&catalog-number=2xxx",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "2xxx",
                          "title": "2xxx"
                      }, ...
                  ],
                  "slug": "catalog-number",
                  "title": "Catalog Number"
              },
              {
                  "items": [
                      {
                          "count": 360,
                          "link": "?q=Software&p=1&evening=Daytime",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "Daytime",
                          "title": "Daytime"
                      },
                      {
                          "count": 76,
                          "link": "?q=Software&p=1&evening=Evening",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "Evening",
                          "title": "Evening"
                      }
                  ],
                  "slug": "evening",
                  "title": "Evening"
              },
              {
                  "items": [
                      {
                          "count": 421,
                          "link": "?q=Software&p=1&instruction-mode=P",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "P",
                          "title": "In Person"
                      },
                      {
                          "count": 13,
                          "link": "?q=Software&p=1&instruction-mode=DL",
                          "removeLink": "?q=Software&p=1",
                          "selected": false,
                          "term": "DL",
                          "title": "Distance Learning"
                      }, ...
                  ],
                  "slug": "instruction-mode",
                  "title": "Instruction Mode"
              }
          ]
        }
          "nextPageLink": "?q=Software&p=2",
          "page": 1,
          "prevPageLink": null,
          "refineQueryTemplate": "q=_QUERY_&p=1",
          "searchTimeMillis": 80,
          "sort": [
              {
                  "direction": "desc",
                  "key": "",
                  "link": "?q=Software&p=1&sort=",
                  "title": "Relevance",
                  "type": "amount"
              },
              {
                  "direction": "asc",
                  "key": "subject",
                  "link": "?q=Software&p=1&sort=subject",
                  "title": "Subject",
                  "type": "alpha"
              },
              {
                  "direction": "desc",
                  "key": "-subject",
                  "link": "?q=Software&p=1&sort=-subject",
                  "title": "Subject",
                  "type": "alpha"
              },
              {
                  "direction": "asc",
                  "key": "catalogNumber",
                  "link": "?q=Software&p=1&sort=catalogNumber",
                  "title": "Catalog Number",
                  "type": "numeric"
              },
              {
                  "direction": "desc",
                  "key": "-catalogNumber",
                  "link": "?q=Software&p=1&sort=-catalogNumber",
                  "title": "Catalog Number",
                  "type": "numeric"
              }
          ],
          "totalItems": 443,
          "totalPages": 3
          }
        }
```
