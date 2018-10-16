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




* **Error Response:**

  Whenever there is an error it will return as follows.

      {
          "status": "failed",
          "message": "Unauthorized Access"
      }





* **Notes:**

  All Request will be allowed based on basic authentication with username and password.
