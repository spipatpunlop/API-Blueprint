FORMAT: 1A
HOST: localhost:4852/v1/sales/

# Amus - Shipping Orders

This is a simple API allowing consumers to view or find or create or delete shipping orders.

## Shipping Orders [/shippingorders]

### All [GET]

+ Request

    + Headers
    
            Authorization: Bearer TOKEN

+ Response 200 (application/json)
    + Attributes (dataItemAndTotal)

+ Response 403 (application/json)
    + Attributes (statusForbidden)
        
### Create [POST]

+ Request (application/json)

    + Headers
    
            Authorization: Bearer TOKEN

    + body

            {
                "shippingDate": "2018-12-05T15:00:00Z",
                "product": {
                    "id": 10233
                },
                "salesOrder": {
                    "id": 492,
                    "orderNumber": "76532-28"
                },
                "qty": 500,
                "price": 5251,
                "destination": "藤商事",
                "notes": "初回納品",
                "location": {
                    "store": null,
                    "code": "02"
                }
            }

+ Response 200 (appication/json)
    + Attributes (dataItemAndUserAC)

### Delete [DELETE]

+ Request (application/json)

    + Headers
    
            Authorization: Bearer TOKEN

    + body

            {
                "data": [
                    {
                        "id": 1,
                        "version": 0
                    },
                    {
                        "id": 2,
                        "version": 0
                    }
                ]
            }

+ Response 200 (application/json)
    + Attributes (deletedResults)
        
+ Response 404 (application/json)
    + Attributes (deletedResults)

+ Response 409 (application,json)
    + Attributes (deletedResults)

## Get Shipping Order By Id [/shippingorders/{id}]

### Get [GET]

+ Parameters
    + id (number) - Id of Shipping Order in the form of long
    
+ Request

    + Headers
    
            Authorization: Bearer TOKEN

+ Response 200 (application/json)
    + Attributes (dataItemAndUserAC)
        
## Sorting Shipping Orders [/shippingorders{?sort}{?dir}]

### Sort [GET]

+ Parameters
    + sort (string) - Item name of sorting
    + dir (string) - Direction od sorting (ascend/descend)

+ Request

    + Headers
                
            Authorization: Bearer TOKEN

+ Response 200 (application/json)
    + Attributes (dataItemAndTotal)
        
## Find Shipping Orders by keyword [/shippingorders{?keyword}]

### Find [GET]

+ Parameters
    + keyword (string) - keyword

+ Request

    + Headers
        
            Authorization: Bearer TOKEN

+ Response 200 (application/json)
    + Attributes (dataItemAndTotal)

## Data Structures

### dataItemAndTotal
    + data: `data` (array) - Collections of Data
    + total: `total` (number) - number of total records
    
### dataItemAndUserAC
    + doc: `doc` (array) - Data details
    + userAC: `userAC` (array) - User account details

### statusForbidden
    + code: 403 (number) - Status Code
    + status: `error` (string) - Status
    + message: `message` (string) - Error message

### deletedResults
    + result: `result` (array) - Result details