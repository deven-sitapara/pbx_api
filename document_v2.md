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
                      "ex_id": "61",
                      "ex_name": "Jessica Holdcroft (Desk Phone)",
                      "ex_number": "1222"
                  },
                  {
                      "ex_id": "49",
                      "ex_name": "Xander Robar (Softphone - Mobile)",
                      "ex_number": "1223"
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
 
* **Notes:**

  All Request will be allowed based on basic authentication with username and password.
