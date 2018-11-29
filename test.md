FORMAT: 1A
HOST: localhost:4852/v1/sales/

# Amus - Shipping Orders

This is a simple API allowing consumers to view or find or create or delete shipping orders.

## Shipping Orders [/shippingorders]

### All [GET]

+ Request

    + Headers
    
            Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCIsImtpZCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCJ9.eyJpc3MiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIiLCJhdWQiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIvcmVzb3VyY2VzIiwiZXhwIjoxNTQ0ODUyNjU0LCJuYmYiOjE1NDIyNjA2NTQsImNsaWVudF9pZCI6ImsxMC5wb3N0bWFuLnN1dmltb25fcGlwYXRwdW5sb3AiLCJjbGllbnRfdHlwZSI6ImhlYWRsZXNzIiwic3ViIjoiMTgxZGIzZjAtNGM0NC00ZDM2LTlkNWMtYWE5MmFlODFhOTk3IiwicHJlZmVycmVkX3VzZXJuYW1lIjoic3V2aW1vbl9waXBhdHB1bmxvcCIsInNjb3BlIjoibWVtYmVyIn0.Dr2zapiKIJVLfn2uixIdMje4xQqLpygyKNG-2n9s6XLg3jKn0wHaQEBSx51a5I5uNKIwCZIlc29eFwiAgWEX3xggmkLVNHIgnTDbUytz64n5SY0k5NZ0i5IGem96CS_GMfVy0B1kgQ9IdZqKdwk2bmERykbZBuWeF7glV3MyLVrEyncHObpcwZ0y-auiPOmShlUbUsyAyODQRiwAyU7XvTbHxswXWcNauxIZx1JEG3yM_7eLmGZAFAV1qL-BFNULkAK6FOWkWb1ItVEg1DSsYYZgSqzenv8Lk5S8sNukM3d8pItVohv9RWU8Ot9q28x38VArocjEQYgQBYmB8sgfUA

+ Response 200 (application/json)
    + Attributes (dataItemAndTotal)

+ Response 403 (application/json)
    + Attributes (statusFrobidden)
        
### Create [POST]

+ Request (application/json)

    + Headers
    
            Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCIsImtpZCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCJ9.eyJpc3MiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIiLCJhdWQiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIvcmVzb3VyY2VzIiwiZXhwIjoxNTQ0ODUyNjU0LCJuYmYiOjE1NDIyNjA2NTQsImNsaWVudF9pZCI6ImsxMC5wb3N0bWFuLnN1dmltb25fcGlwYXRwdW5sb3AiLCJjbGllbnRfdHlwZSI6ImhlYWRsZXNzIiwic3ViIjoiMTgxZGIzZjAtNGM0NC00ZDM2LTlkNWMtYWE5MmFlODFhOTk3IiwicHJlZmVycmVkX3VzZXJuYW1lIjoic3V2aW1vbl9waXBhdHB1bmxvcCIsInNjb3BlIjoibWVtYmVyIn0.Dr2zapiKIJVLfn2uixIdMje4xQqLpygyKNG-2n9s6XLg3jKn0wHaQEBSx51a5I5uNKIwCZIlc29eFwiAgWEX3xggmkLVNHIgnTDbUytz64n5SY0k5NZ0i5IGem96CS_GMfVy0B1kgQ9IdZqKdwk2bmERykbZBuWeF7glV3MyLVrEyncHObpcwZ0y-auiPOmShlUbUsyAyODQRiwAyU7XvTbHxswXWcNauxIZx1JEG3yM_7eLmGZAFAV1qL-BFNULkAK6FOWkWb1ItVEg1DSsYYZgSqzenv8Lk5S8sNukM3d8pItVohv9RWU8Ot9q28x38VArocjEQYgQBYmB8sgfUA

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

        {
            "doc": {
            "shippingDate": "2018-12-05T15:00:00Z",
            "product": {
                "id": 10233,
                "itemName": "A64 液晶演出制御基板(DE1601B/D1401C/E1403C)(完)D/Eﾘﾕｰｽ",
                "relatedItemCode": "12DA611HD168",
                "relatedItemName": "A64 DE601B/D-R/E-R",
                "productFamily": "A64DR",
                "customerItemCode": "2600651032"
            },
            "qty": 500,
            "price": 5251,
            "amount": 2625500,
            "destination": "藤商事",
            "notes": "初回納品",
            "salesOrder": {
                "id": 492,
                "orderNumber": "76532-28"
            },
            "location": {
                "store": null,
                "code": "02"
            },
            "id": 25,
            "version": 0,
            "createdAt": "2018-11-28T17:46:18.5059789+09:00",
            "createdBy": {
                "userId": "suvimon_pipatpunlop",
                "userName": "Pipatpunlop Suvimon"
            },
            "modifiedAt": "2018-11-28T17:46:18.5059789+09:00",
            "deletedAt": null,
            "deletedBy": null,
            "readers": [],
            "editors": []
            },
            "userAC": {
                "userId": "suvimon_pipatpunlop",
                "userName": "Pipatpunlop Suvimon",
                "userDeptCode": "19",
                "userDeptName": "情報システム部",
                "userGroupCode": "19A",
                "userGroupName": "-",
                "userPostCode": 0,
                "userPostName": "-",
                "roles": [
                    "Admin"
                ],
                "accessLevel": 3,
                "userGroups": [],
                "canCreate": true,
                "canDelete": true,
                "canAddAttachment": true,
                "canDeleteAttachment": true,
                "canEdit": true
            }
        }

### Delete [DELETE]

+ Request (application/json)

    + Headers
    
            Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCIsImtpZCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCJ9.eyJpc3MiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIiLCJhdWQiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIvcmVzb3VyY2VzIiwiZXhwIjoxNTQ0ODUyNjU0LCJuYmYiOjE1NDIyNjA2NTQsImNsaWVudF9pZCI6ImsxMC5wb3N0bWFuLnN1dmltb25fcGlwYXRwdW5sb3AiLCJjbGllbnRfdHlwZSI6ImhlYWRsZXNzIiwic3ViIjoiMTgxZGIzZjAtNGM0NC00ZDM2LTlkNWMtYWE5MmFlODFhOTk3IiwicHJlZmVycmVkX3VzZXJuYW1lIjoic3V2aW1vbl9waXBhdHB1bmxvcCIsInNjb3BlIjoibWVtYmVyIn0.Dr2zapiKIJVLfn2uixIdMje4xQqLpygyKNG-2n9s6XLg3jKn0wHaQEBSx51a5I5uNKIwCZIlc29eFwiAgWEX3xggmkLVNHIgnTDbUytz64n5SY0k5NZ0i5IGem96CS_GMfVy0B1kgQ9IdZqKdwk2bmERykbZBuWeF7glV3MyLVrEyncHObpcwZ0y-auiPOmShlUbUsyAyODQRiwAyU7XvTbHxswXWcNauxIZx1JEG3yM_7eLmGZAFAV1qL-BFNULkAK6FOWkWb1ItVEg1DSsYYZgSqzenv8Lk5S8sNukM3d8pItVohv9RWU8Ot9q28x38VArocjEQYgQBYmB8sgfUA

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

        {
            "result": {
                "succeeded": [
                    {
                        "id": 1
                    }
                ]
            }
        }
        
+ Response 404 (application/json)

        {
            "message": "削除できません。"
        }

+ Response 409 (application,json)

        {
            "message": "一部のデータ削除に失敗しました。ご確認ください。",
            "result": {
                "succeeded": [
                    {
                        "id": 1
                    }
                ],
                "failed": [
                    {
                        "id": 2
                    }
                ]
            }
        }

## Get Shipping Order By Id [/shippingorders/{id}]

### Get [GET]

+ Parameters
    + id (number) - Id of Shipping Order in the form of long
    
+ Request

    + Headers
    
            Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCIsImtpZCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCJ9.eyJpc3MiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIiLCJhdWQiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIvcmVzb3VyY2VzIiwiZXhwIjoxNTQ0ODUyNjU0LCJuYmYiOjE1NDIyNjA2NTQsImNsaWVudF9pZCI6ImsxMC5wb3N0bWFuLnN1dmltb25fcGlwYXRwdW5sb3AiLCJjbGllbnRfdHlwZSI6ImhlYWRsZXNzIiwic3ViIjoiMTgxZGIzZjAtNGM0NC00ZDM2LTlkNWMtYWE5MmFlODFhOTk3IiwicHJlZmVycmVkX3VzZXJuYW1lIjoic3V2aW1vbl9waXBhdHB1bmxvcCIsInNjb3BlIjoibWVtYmVyIn0.Dr2zapiKIJVLfn2uixIdMje4xQqLpygyKNG-2n9s6XLg3jKn0wHaQEBSx51a5I5uNKIwCZIlc29eFwiAgWEX3xggmkLVNHIgnTDbUytz64n5SY0k5NZ0i5IGem96CS_GMfVy0B1kgQ9IdZqKdwk2bmERykbZBuWeF7glV3MyLVrEyncHObpcwZ0y-auiPOmShlUbUsyAyODQRiwAyU7XvTbHxswXWcNauxIZx1JEG3yM_7eLmGZAFAV1qL-BFNULkAK6FOWkWb1ItVEg1DSsYYZgSqzenv8Lk5S8sNukM3d8pItVohv9RWU8Ot9q28x38VArocjEQYgQBYmB8sgfUA

+ Response 200 (application/json)

        {
            "doc": {
                "shippingDate": "2018-10-04T15:00:00Z",
                "product": {
                    "id": 10123,
                    "itemName": "ｴｺ D41 液晶演出制御基板(DE1404A/D1401C/E1403C)(完)",
                    "relatedItemCode": "12DA361HD146",
                    "relatedItemName": "D41 ｴｺﾓｸｼ D/DE/ E",
                    "productFamily": "D41D",
                    "customerItemCode": "4500890012"
                },
                "qty": 200,
                "price": 2994,
                "amount": 598800,
                "destination": "藤商事",
                "notes": "初回納品",
                "salesOrder": {
                    "id": 10,
                    "orderNumber": "73138-5"
                },
                "location": {
                    "store": null,
                    "code": "02"
                },
                "id": 4,
                "version": 0,
                "createdAt": "2018-11-16T07:21:53.935Z",
                "createdBy": {
                    "userId": "suvimon_pipatpunlop",
                    "userName": "Pipatpunlop Suvimon"
                },
                "modifiedAt": "2018-11-16T07:21:53.935Z",
                "deletedAt": null,
                "deletedBy": null,
                "readers": [],
                "editors": []
            },
            "userAC": {
                "userId": "suvimon_pipatpunlop",
                "userName": "Pipatpunlop Suvimon",
                "userDeptCode": "19",
                "userDeptName": "情報システム部",
                "userGroupCode": "19A",
                "userGroupName": "-",
                "userPostCode": 0,
                "userPostName": "-",
                "roles": [
                    "Admin"
                ],
                "accessLevel": 3,
                "userGroups": [],
                "canCreate": true,
                "canDelete": true,
                "canAddAttachment": true,
                "canDeleteAttachment": true,
                "canEdit": true
            }
        }
        
## Sorting Shipping Orders [/shippingorders{?sort}{?dir}]

### Sort [GET]

+ Parameters
    + sort (string) - Item name of sorting
    + dir (string) - Direction od sorting (ascend/descend)

+ Request

    + Headers
                
            Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCIsImtpZCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCJ9.eyJpc3MiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIiLCJhdWQiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIvcmVzb3VyY2VzIiwiZXhwIjoxNTQ0ODUyNjU0LCJuYmYiOjE1NDIyNjA2NTQsImNsaWVudF9pZCI6ImsxMC5wb3N0bWFuLnN1dmltb25fcGlwYXRwdW5sb3AiLCJjbGllbnRfdHlwZSI6ImhlYWRsZXNzIiwic3ViIjoiMTgxZGIzZjAtNGM0NC00ZDM2LTlkNWMtYWE5MmFlODFhOTk3IiwicHJlZmVycmVkX3VzZXJuYW1lIjoic3V2aW1vbl9waXBhdHB1bmxvcCIsInNjb3BlIjoibWVtYmVyIn0.Dr2zapiKIJVLfn2uixIdMje4xQqLpygyKNG-2n9s6XLg3jKn0wHaQEBSx51a5I5uNKIwCZIlc29eFwiAgWEX3xggmkLVNHIgnTDbUytz64n5SY0k5NZ0i5IGem96CS_GMfVy0B1kgQ9IdZqKdwk2bmERykbZBuWeF7glV3MyLVrEyncHObpcwZ0y-auiPOmShlUbUsyAyODQRiwAyU7XvTbHxswXWcNauxIZx1JEG3yM_7eLmGZAFAV1qL-BFNULkAK6FOWkWb1ItVEg1DSsYYZgSqzenv8Lk5S8sNukM3d8pItVohv9RWU8Ot9q28x38VArocjEQYgQBYmB8sgfUA

+ Response 200 (application/json)

        {
            "total":  393,
            "data": [
                {
                    "id": 123,
                    "shippingDate": "2018-12-05T15:00:00Z",
                    "product": {
                        "id": 10233,
                         "itemName": "A64 液晶演出制御基板(DE1601B/D1401C/E1403C)(完)D/Eﾘﾕｰｽ",
                         "relatedItemCode": "12DA611HD168",
                         "relatedItemName": "A64 DE601B/D-R/E-R",
                         "productFamily": "A64",
                         "customerItemCode": "2600651032"
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
                },
                {
                    "id": 12,
                    "shippingDate": "2017-19-05T15:00:00Z",
                    "product": {
                        "id": 12273,
                         "itemName": "A64 液晶演出制御基板(DE1601B/D1401C/E1403C)(完)D/Eﾘﾕｰｽ",
                         "relatedItemCode": "12DA611HD168",
                         "relatedItemName": "A64 DE601B/D-R/E-R",
                         "productFamily": "A64",
                         "customerItemCode": "2600651032"
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
                },
            ]
        }
        
## Find Shipping Orders by keyword [/shippingorders{?keyword}]

### Find [GET]

+ Parameters
    + keyword (string) - keyword

+ Request

    + Headers
        
            Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCIsImtpZCI6ImNncXVvMElCVm52UTZyMnp6TktGSU9yZWdHOCJ9.eyJpc3MiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIiLCJhdWQiOiJodHRwczovL2sxMC5zdW4tZGVuc2hpLmNvLmpwL2lkcDIvcmVzb3VyY2VzIiwiZXhwIjoxNTQ0ODUyNjU0LCJuYmYiOjE1NDIyNjA2NTQsImNsaWVudF9pZCI6ImsxMC5wb3N0bWFuLnN1dmltb25fcGlwYXRwdW5sb3AiLCJjbGllbnRfdHlwZSI6ImhlYWRsZXNzIiwic3ViIjoiMTgxZGIzZjAtNGM0NC00ZDM2LTlkNWMtYWE5MmFlODFhOTk3IiwicHJlZmVycmVkX3VzZXJuYW1lIjoic3V2aW1vbl9waXBhdHB1bmxvcCIsInNjb3BlIjoibWVtYmVyIn0.Dr2zapiKIJVLfn2uixIdMje4xQqLpygyKNG-2n9s6XLg3jKn0wHaQEBSx51a5I5uNKIwCZIlc29eFwiAgWEX3xggmkLVNHIgnTDbUytz64n5SY0k5NZ0i5IGem96CS_GMfVy0B1kgQ9IdZqKdwk2bmERykbZBuWeF7glV3MyLVrEyncHObpcwZ0y-auiPOmShlUbUsyAyODQRiwAyU7XvTbHxswXWcNauxIZx1JEG3yM_7eLmGZAFAV1qL-BFNULkAK6FOWkWb1ItVEg1DSsYYZgSqzenv8Lk5S8sNukM3d8pItVohv9RWU8Ot9q28x38VArocjEQYgQBYmB8sgfUA

+ Response 200 (application/json)
    + Attributes (dataItemAndTotal)

## Data Structures

### dataItemAndTotal
    + data: `data` (array) - Collections of Data
    + total: `total` (number) - number of total records

### statusFrobidden
    + code: 403 (number) - Status Code
    + status: `error` (string) - Status
    + message: `message` (string) - Error message
