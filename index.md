swagger: '2.0'
info:
  version: '1.0.0'
  title: Centify API
  description: >
    Test description.
host: centify.com
basePath: /api.centify.com/
schemes:
  - http
consumes:
  * application/json
produces:
  * application/json
paths:
  /v:version/signup:
    post:
      tags:
        - Signup
      summary: Signup to Centify
      description: >
        Create a new Centify account.
      produces:
        * application/json
	* application/xml
	* text/xml
	* text/html
      parameters:
        * name: FirstName
	  in: query
	  required: true
	  type: string
      responses:
        '200':
	  description: Created
	  schema:
	    properties:
	      Location:
	        type: https://api.centify.com/v1/orgs/:id