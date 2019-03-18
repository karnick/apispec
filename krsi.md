FORMAT: 1A

# KRSI

An application that empowers farmers, by making their finacally smart!! An application that empowers farmers, by making their finacally smart!! **[KRSI](https://www.krsi.org)** is app that make it possible.

## Users Collection [/users]

User and profile details can be achieved using these APIs.

### List All Users [GET]


+ Response 200 (application/json)

        [
            {
                "name": "Karthik Sriram",
                "email": "bglkarthik@yahoo.co.in"
                "created": "2015-08-05T08:40:51.620Z",
                "modified": "2019-08-05T08:40:51.620Z",
                "uuid": "SWERLW12323SDEERMXY"
                "signupDate": "2015-08-05T08:40:51.620Z"

                "farms": [
                        {
                            "name": "Mango Farm",
                            "acres": 2048
                        }, {
                            "name": "Rice Farm 2",
                            "acres": 1024
                        }, {
                            "choice": "Poultary Farm",
                            "acres": 512
                        }
                ]
            },
            {
                "name": "Thajith",
                "email": "Thajith@yahoo.co.in"
                "created": "2014-12-05T18:40:51.620Z",
                "modified": "2018-08-06T08:30:31.620Z",
                "uuid": "SWERLW12323STATCHI"
                "signupDate": "2015-08-05T08:40:51.620Z"

                "farms": [
                        {
                            "name": "Apple Farm",
                            "acres": 21
                        }, {
                            "name": "Wheat Farm 2",
                            "acres": 414
                        }, {
                            "choice": "Fish Farm",
                            "acres": 512
                        }
                ]
            }
        ]
        
        
## User [/users/{uuid}]

User details can be fetched by passing uuid.

### Details of a User [GET]

Get List of all Users

+ Parameters
    + uuid (string) - pass the uuid to be deleted

+ Response 200 (application/json) 
        
        {
            "name": "Karthik Sriram",
            "email": "bglkarthik@yahoo.co.in"
            "created": "2015-08-05T08:40:51.620Z",
            "modified": "2019-08-05T08:40:51.620Z",
            "uuid": "SWERLW12323SDEERMXY"
            "signupDate": "2015-08-05T08:40:51.620Z"

            "farms": [
                {
                    "name": "Mango Farm",
                    "acres": 2048
                }, {
                    "name": "Rice Farm 2",
                    "acres": 1024
                }, {
                    "choice": "Poultary Farm",
                    "acres": 512
                }
            ]
        }

+ Response 404 (text/plain)

        There is no such user
    

### Delete a User [DELETE]

Delete the user by passing the uuid of the user.

+ Parameters
    + uuid (string) - pass the uuid to be deleted

+ Response 204 

### Create a User  [POST]

You may create your own question using this action. It takes a JSON
object containing a question and a collection of answers in the
form of choices.

+ Request (application/json)

    + Body
        
            {
                 "name": "Karthik Sriram",
                 "signUpDate": "2019-03-05T08:40:51.620Z",
                 "email":
            }

+ Response 201 (application/json)

    + Headers

            Location: /questions/2

    + Body

            {
                "name": "Karthik Sriram",
                "signUpDate": "2019-03-05T08:40:51.620Z",
                "email":
            }


