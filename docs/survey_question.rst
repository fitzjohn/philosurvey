****************
 SURVEY QUESTION
****************

CREATE
======
Request
-------
Method: POST
````````````
URL
'''
/api/v1/survey_questions

Payload
'''''''
The payload of the request must be submitted as valid JSON using the following format.

.. code-block:: javascript

     {
         “value”: “[quest string]”,
         “class_id”: “[quest class id 1],[quest class id 2]”,
         “type”: {“kind”:”[Standard|Custom]”,”id”:“[quest type id]”},
         “survey_order”: “[quest survey order number]”,        
         “group_id”: “[quest group id]”,
         “tags” : {
            “[key1]”: “”,
            “[key2]”: “[value2]”,
            “[key3]”: “[value3,value4,value5]”
      }
Method: GET
````````````
URL
'''
/api/v1/survey_questions?method=post&...

Payload
'''''''
There is no payload beyond the query string itself.

Response
--------
Status: 200
```````````
Payload
'''''''
The payload of the response will be valid JSON using the following format.

.. code-block:: javascript

   { 
      "meta": {
      },
      “survey_question”: {
         “value”: “[quest string]”,                    //Note: May not want to make this externally visible.
         “hash”: “[quest hash]”,
         “class_id”: “[quest class id 1],[quest class id 2]”,
         “type”: {“kind”:”[Standard|Custom]”,”id”:“[quest type id]”},
         “survey_order”: “[quest survey order number]”,        //Note: Only has meaning within a survey.
         “response_order”: “[quest response order number]”,    //Note: Only has meaning within a survey response.
         “group_id”: “[quest group id]”,
         “tags” : {
            “[key1]”: “”,
            “[key2]”: “[value2]”,
            “[key3]”: “[value3,value4,value5]”
      },
      "notifications":{
      }
   }

Status: 500
```````````
Payload
'''''''
The payload of the response will be valid JSON using the following format.

.. code-block:: javascript

   { 
      "meta": {
      },
      “survey_question”: {
      },
      "notifications":{
      }
   }

View
====

Request
-------

Response
--------

Update
======

Request
-------

Response
--------

Delete
======

Request
-------

Response
--------
