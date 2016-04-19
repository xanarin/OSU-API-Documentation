# Dining API Specification

## API Endpoint
The API endpoint as of April 19, 2016 is https://content.osu.edu/v2/api/v1/dining

## Retrieving Location Information

#### Query
List of dining locations and information can be requested by appending the path '/locations/menus' to the endpoint. For example:
```
https://content.osu.edu/v2/api/v1/dining/locations/menus
```

Note, by querying the URL:
```
https://content.osu.edu/v2/api/v1/dining/locations
```
A similar response is given, except that the menu information is not included for each location.

#### Sample Response
_Ellipses mark possible repetition_
```json
{
    "data": {
        "locationsMenus": [
            {
                "address1": "1858 Neil Ave Mall",
                "address2": "",
                "campusBuildingID": "050",
                "city": "Columbus",
                "cuisines": [
                    {
                        "cuisineType": "Deli-Style Sandwiches"
                    },
                    {
                        "cuisineType": "Salad"
                    },
                    {
                        "cuisineType": "Specialty Coffees"
                    },
                    {
                        "cuisineType": "Yogurt/Fruit"
                    }
                ],
                "diningStyle": "Cafe/Grab 'n Go",
                "iconUrl": "https://dining.osu.edu/NetNutritionimages/coffee.gif",
                "id": 101,
                "itemHash": "6433907e1dc8cc97fe2be2f0a92dbd3f",
                "locationMenu": [
                    {
                        "isDaySpecificMenu": false,
                        "menuDate": null,
                        "sections": [
                            {
                                "menuSectionName": "Daily Menu",
                                "order": 1,
                                "sectionID": 101
                            }
                        ]
                    }
                ],
                "locationName": "Berry Cafe",
                "photoUrl": null,
                "state": "OH",
                "summary": "Drag your tired body down to the first floor of the Thompson Library.  Grab a fresh sandwich and chips, or a fruit parfait and a cookie, or just go straight for the caffeine with our TBC Mocha.  All you need to help you succeed",
                "thumbnailUrl": null,
                "zip": "43210"
            },
            {
                "address1": "1900 Cannon Drive",
                "address2": "",
                "campusBuildingID": "272",
                "city": "Columbus",
                "cuisines": [],
                "diningStyle": null,
                "iconUrl": "https://dining.osu.edu/NetNutritionimages/salad.gif",
                "id": 127,
                "itemHash": "7051482eacbe55e412afd1c9668bbee7",
                "locationMenu": [
                    {
                        "isDaySpecificMenu": false,
                        "menuDate": null,
                        "sections": [
                            {
                                "menuSectionName": "Daily Menu",
                                "order": 1,
                                "sectionID": 157
                            }
                        ]
                    }
                ],
                "locationName": "Morrill C-Store",
                "photoUrl": null,
                "state": "OH",
                "summary": "On any given day at Morrill C-Store, you can make your own MOCO Fusion bowl, salad, or wrap, and purchase an assortment of quick, pick-up selections.",
                "thumbnailUrl": null,
                "zip": "43210"
            },...
        ]
    },
    "lastModified": "2016-04-19T14:53:06.467Z",
    "status": "success"
}
```

## Retrieving Foods for each Location

#### Query
List of dining locations and information can be requested by appending the path '/full/menu/section' and the **sectionID** number given by locationMenu field for each location in the location request listed above. For example:
```
https://content.osu.edu/v2/api/v1/dining/full/menu/section/101
```
Lists the menu for the "Daily Menu" at the Berry Cafe.

#### Sample Result
_Ellipses mark possible repetition_
```json
{
    "data": {
        "fullMenu": [
            {
                "course": "Limited Time Offer",
                "id": 107,
                "itemHash": "676c01c17b71bd93cf3b610a760c58b4",
                "name": "Fruit Tart",
                "nutrition": [
                    {
                        "displayQuantity": true,
                        "name": "Calories",
                        "percentOfGoal": 14,
                        "quantity": 282,
                        "sortOrder": 1,
                        "unitOfMeasure": ""
                    },
                    {
                        "displayQuantity": true,
                        "name": "Total Fat",
                        "percentOfGoal": 17,
                        "quantity": 11,
                        "sortOrder": 3,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Saturated Fat",
                        "percentOfGoal": 28,
                        "quantity": 6,
                        "sortOrder": 4,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Trans Fat",
                        "percentOfGoal": 3,
                        "quantity": 0,
                        "sortOrder": 5,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Cholesterol",
                        "percentOfGoal": 22,
                        "quantity": 66,
                        "sortOrder": 6,
                        "unitOfMeasure": "mg"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Sodium",
                        "percentOfGoal": 5,
                        "quantity": 110,
                        "sortOrder": 7,
                        "unitOfMeasure": "mg"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Total Carbohydrate",
                        "percentOfGoal": 13,
                        "quantity": 40,
                        "sortOrder": 8,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Dietary Fiber",
                        "percentOfGoal": 9,
                        "quantity": 2,
                        "sortOrder": 9,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Sugars",
                        "percentOfGoal": 0,
                        "quantity": 18.5,
                        "sortOrder": 10,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": true,
                        "name": "Protein",
                        "percentOfGoal": 11,
                        "quantity": 5.5,
                        "sortOrder": 11,
                        "unitOfMeasure": "Gram"
                    },
                    {
                        "displayQuantity": false,
                        "name": "Vitamin A",
                        "percentOfGoal": 3,
                        "quantity": 0,
                        "sortOrder": 12,
                        "unitOfMeasure": ""
                    },
                    {
                        "displayQuantity": false,
                        "name": "Vitamin C",
                        "percentOfGoal": 15,
                        "quantity": 0,
                        "sortOrder": 13,
                        "unitOfMeasure": ""
                    },
                    {
                        "displayQuantity": false,
                        "name": "Calcium",
                        "percentOfGoal": 7,
                        "quantity": 0,
                        "sortOrder": 14,
                        "unitOfMeasure": ""
                    },
                    {
                        "displayQuantity": false,
                        "name": "Iron",
                        "percentOfGoal": 12,
                        "quantity": 0,
                        "sortOrder": 15,
                        "unitOfMeasure": ""
                    }
                ],
                "portionSize": "Each",
                "price": 0,
                "sortOrder": 1,
                "traits": [
                    {
                        "category": "Allergen",
                        "name": "Dairy"
                    },
                    {
                        "category": "Allergen",
                        "name": "Eggs"
                    },
                    {
                        "category": "Allergen",
                        "name": "Gluten"
                    },
                    {
                        "category": "Allergen",
                        "name": "Soy"
                    },
                    {
                        "category": "Requirement",
                        "name": "Vegetarian"
                    },
                    {
                        "category": "Allergen",
                        "name": "Wheat"
                    }
                ]
            },...
          ]
      },
      "lastModified": "2016-04-19T08:02:59.360Z",
      "status": "success"
}
```
_Note: These responses are **very** large, so take care when requesting and parsing this data_
