# API Documentation #

* **URL**

  https://{yourdomain.com}/user/login

* **Method:**
  GET

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": {
              "user_id": "579"
          }
      }
* **Error Response:**

  Whenever there is an error it will return as follows.

      {
          "status": "failed",
          "message": "Unauthorized Access"
      }


* **URL**

  https://{yourdomain.com}/user/get

* **Method:**
  GET

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "us_id": "97",
                  "us_username": "admin"
              },
              {
                  "us_id": "134",
                  "us_username": "advicewise"
              },
              {
                  "us_id": "124",
                  "us_username": "Airlord"
              },
            ]
      }
* **Error Response:**

  Whenever there is an error it will return as follows.

      {
          "status": "failed",
          "message": "Unauthorized Access"
      }

* **URL**

  https://{yourdomain.com}/user/tenants

* **Method:**
  POST

* **Perameter:**
  user: EmailAddress

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": {
              "user_id": "134",
              "tenants": [
                  {
                      "te_id": "80",
                      "te_name": "Advice Wise Solicitors"
                  }
              ]
          }
      }
* **Error Response:**

  Whenever there is an error it will return as follows.

      {
          "status": "failed",
          "message": "Unauthorized Access"
      }

* **URL**

  https://{yourdomain.com}/destination/all

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          {
              "status": "success",
              "data": [
                  {
                      "de_id": "156",
                      "de_type_src": "CONDITION",
                      "de_type_dst": "DISA",
                      "de_ord": "1"
                  },
                  {
                      "de_id": "157",
                      "de_type_src": "NOTCONDITION",
                      "de_type_dst": "CONDITION",
                      "de_ord": "1"
                  },
              ]
          }
      }
* **Error Response:**

  Whenever there is an error it will return as follows.

      {
          "status": "failed",
          "message": "Unauthorized Access"
      }

* **URL**

  https://{yourdomain.com}/extension/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "ex_id": "11",
                  "ex_name": "Chris Latremoille",
                  "ex_number": "221",
                  "ex_cidnum": "15146339933",
                  "ex_cidname": "Uniglobe Dorval",
                  "ex_callwaiting": ""
              },
              {
                  "ex_id": "12",
                  "ex_name": "Francine Girard",
                  "ex_number": "222",
                  "ex_cidnum": "15146339933",
                  "ex_cidname": "Uniglobe Dorval",
                  "ex_callwaiting": ""
              },
                  ]
          }
      }


* **URL**

  https://{yourdomain.com}/extension/byid

* **Method:**
  POST

* **Perameter:**
  extension_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "ex_id": "240",
                  "ex_name": "Test",
                  "ex_number": "251",
                  "ex_cidnum": "",
                  "ex_cidname": "Test",
                  "ex_callwaiting": ""
              }
          ]
      }


* **URL**

  https://{yourdomain.com}/extension/user

* **Method:**
  POST

* **Perameter:**
  tenant_id:
  extension_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "name": "251-UniglobeDorval",
                  "host": "dynamic",
                  "secret": "$50jLkuPLypGxqBmyftPV51AM91."
              }
          ]
      }



* **URL**

  https://{yourdomain.com}/extension/usersecret

* **Method:**
  POST

* **Perameter:**
  tenant_id:
  extension_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": "$aLRMruPLypGxqBmyftPV5FPJ3I."
      }


* **URL**

  https://{yourdomain.com}/extension/getCidNumber

* **Method:**
  POST

* **Perameter:**
  extension_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": "15146339933"
      }


* **URL**

  https://{yourdomain.com}/extension/getCidNumberList

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "ex_cidnum": "15146339933"
              },
              {
                  "ex_cidnum": "15146339933"
              },
              {
                  "ex_cidnum": "15146339933"
              },
              {
                  "ex_cidnum": "15146339933"
              },
          ]
      }




* **URL**

  https://{yourdomain.com}/extension/GetFMFCallerId

* **Method:**
  POST

* **Perameter:**
  extension_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": "15146339933"
      }


* **URL**

  https://{yourdomain.com}/extension/GetFMFCallerIdList

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "GetFMFCallerId": "15146339933"
              },
              {
                  "GetFMFCallerId": "15146339933"
              },
              {
                  "GetFMFCallerId": "15146339933"
              },
              {
                  "GetFMFCallerId": "15146339933"
              },
          ]
      }


* **URL**

  https://{yourdomain.com}/did/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "di_id": "2",
                  "di_country": "",
                  "di_area": "",
                  "di_number": "15146001434",
                  "di_comment": ""
              },
              {
                  "di_id": "3",
                  "di_country": "",
                  "di_area": "",
                  "di_number": "14388197387",
                  "di_comment": ""
              },
              {
                  "di_id": "30",
                  "di_country": "",
                  "di_area": "",
                  "di_number": "15146339933",
                  "di_comment": "Uniglobe Dorval - Main"
              }
          ]
      }


* **URL**

  https://{yourdomain.com}/did/byid

* **Method:**
  POST

* **Perameter:**
  did_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**


     {
         "status": "success",
         "data": [
             {
                 "di_te_id": "2",
                 "di_country": "",
                 "di_area": "",
                 "di_number": "12894701289",
                 "di_comment": "OnSwitch - Canada - Ontario - Newmarket",
                 "di_recording": "yes",
                 "di_fax": "no",
                 "di_didprefix": "",
                 "di_didnameprefix": ""
             }
         ]
     }



* **URL**

  https://{yourdomain.com}/hunt/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

      {
          "status": "success",
          "data": [
              {
                  "hu_id": "3",
                  "hu_number": "501",
                  "hu_name": "Franchise Opportunities",
                  "hu_type": "RINGALL",
                  "hu_ringtime": "60"
              },
              {
                  "hu_id": "4",
                  "hu_number": "502",
                  "hu_name": "General Inquriies",
                  "hu_type": "RINGALL",
                  "hu_ringtime": "60"
              }
          ]
      }


* **URL**

  https://{yourdomain.com}/hunt/byid


* **Method:**
  POST

* **Perameter:**
  hunt_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**


     {
         "status": "success",
         "data": [
             {
                 "hu_id": "4",
                 "hu_number": "502",
                 "hu_name": "General Inquriies",
                 "hu_type": "RINGALL",
                 "hu_ringtime": "60",
                 "hu_checkinuse": ""
             }
         ]
     }


* **URL**

  https://{yourdomain.com}/hunt/deletebyid

* **Method:**
  POST

* **Perameter:**
  hunt_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": "Record Deleted Successfully."
     }

* **Error Response:**

     {
         "status": "failed",
         "message": "Record Not Found."
     }


* **URL**

  https://{yourdomain.com}/phone/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": [
             {
                 "ph_id": "1",
                 "ph_name": "asdas",
                 "ph_te_id": "1",
                 "ph_pm_id": "1",
                 "ph_mac": "asd",
                 "ph_filename": "asdasd"
             }
         ]
     }


* **URL**

  https://{yourdomain.com}/phone/deletebyid

* **Method:**
  POST

* **Perameter:**
  phone_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": "Record Deleted Successfully."
     }

* **Error Response:**

     {
         "status": "failed",
         "message": "Record Not Found."
     }


* **URL**

  https://{yourdomain.com}/phone/AddNewPhone

* **Method:**
  POST

* **Perameter:**
  phone:

    Example value: {"ph_name":"xyz","ph_te_id":"1","ph_pm_id":"1","ph_mac":"1.1.25.1","ph_http_user":"abcdasda","ph_http_password":"132456"}

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": {
             "msg": "Record Inserted Successfully.",
             "PhoneID": "4"
         }
     }

* **Error Response:**

    {
        "status": "failed",
        "message": "Please Enter Required Fields."
    }

Required Fields:
ph_name,ph_te_id,ph_pm_id,ph_mac


* **URL**

  https://{yourdomain.com}/hunt/updatebyid

* **Method:**
  POST

* **Perameter:**
  hunt_id:
  hunt:

    Example value hunt: {"hu_number":"111","hu_name":"AAA","hu_type":"AA","hu_ringtime":"2"}

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": {
             "msg": "Record Updated Successfully."
         }
     }

* **Error Response:**

    {
        "status": "failed",
        "message": "Record Not Found."
    }


* **URL**

  https://{yourdomain.com}/did/updatebyid

* **Method:**
  POST

* **Perameter:**
  did_id:
  did:

    Example value did: {"di_number":"1111111","di_didprefix":"12","di_didnameprefix":"asd","di_country":"USA","di_area":"test","di_comment":"Test Comment"}

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": {
             "msg": "Record Updated Successfully."
         }
     }

* **Error Response:**

    {
        "status": "failed",
        "message": "Record Not Found."
    }


* **URL**

  https://{yourdomain.com}/voicemail/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

    {
        "status": "success",
        "data": [
            {
                "uniqueid": "55",
                "context": "EscapeGamesCanada",
                "fullname": "General Delivery Voicemail",
                "email": "info@escapegames.ca"
            }
        ]
    }



* **URL**

  https://{yourdomain.com}/user/updatebyid

* **Method:**
  POST

* **Perameter:**
  user_id:
  password:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

    {
        "status": "success",
        "data": {
            "msg": "Record Updated Successfully."
        }
    }

* **Error Response:**

{
    "status": "failed",
    "message": "Record Not Found."
}




* **URL**

  https://{yourdomain.com}/condition/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

    {
        "status": "success",
        "data": [
            {
                "co_id": "2",
                "co_name": "Chris Latremoille DISA (END OF CHAIN)",
                "co_type": "CALLERID",
                "co_timezone": "",
                "co_param1": "5146349955",
                "co_param2": "5149239933",
                "co_param3": "",
                "co_param4": "",
                "co_param5": "",
                "co_param6": "",
                "co_param7": "",
                "co_param8": "",
                "co_param9": "",
                "co_param10": "",
                "co_param11": "",
                "co_param12": ""
            },
            {
                "co_id": "3",
                "co_name": "Francine Girard DISA",
                "co_type": "CALLERID",
                "co_timezone": "",
                "co_param1": "5148273211",
                "co_param2": "",
                "co_param3": "",
                "co_param4": "",
                "co_param5": "",
                "co_param6": "",
                "co_param7": "",
                "co_param8": "",
                "co_param9": "",
                "co_param10": "",
                "co_param11": "",
                "co_param12": ""
            }
        ]
    }



* **URL**

  https://{yourdomain.com}/ivr/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

    {
        "status": "success",
        "data": [
            {
                "iv_id": "1",
                "iv_name": "Main Menu - FR"
            },
            {
                "iv_id": "4",
                "iv_name": "Main Menu - EN"
            }
        ]
    }



* **URL**

  https://{yourdomain.com}/custom/bytenant

* **Method:**
  POST

* **Perameter:**
  tenant_id:

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

    {
        "status": "success",
        "data": [
            {
                "cu_id": "2",
                "cu_name": "Vickie Kyriakakos Mobile",
                "cu_ct_id": "1",
                "ct_name": "FORWARD",
                "ct_description": "<t>Forward call to</t>"
            }
        ]
    }



* **URL**

  https://{yourdomain.com}/extension/updatebyid

* **Method:**
  POST

* **Perameter:**
  extension_id:
  extension:

    Example value hunt: {"ex_name":"AAA","ex_number":"11","ex_cidnum":"12","ex_cidname":"AAA"}

*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON
* **Success Response:**

     {
         "status": "success",
         "data": {
             "msg": "Record Updated Successfully."
         }
     }

* **Error Response:**

    {
        "status": "failed",
        "message": "Record Not Found."
    }



* **URL**

  https://{yourdomain.com}/cdr/getCallHistory

* **Method:**
  POST

* **Perameter:**
  start_date_ymd:
  end_date_ymd:
  tenant_code
  firstdst
  disposition
  cost


*  **BASIC Auth**
    username:
    password:

* **Output Format**
  JSON




* **Error Response:**

  Whenever there is an error it will return as follows.

      {
          "status": "failed",
          "message": "Unauthorized Access"
      }





* **Notes:**

  All Request will be allowed based on basic authentication with username and password.



