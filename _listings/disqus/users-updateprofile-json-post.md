---
swagger: "2.0"
info:
  title: Disqus
  description: Welcome to the Disqus Web API. The API enables developers to communicate
    with Disqus data from within their own applications.
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? |2-

        /users/updateProfile.json
  : post:
      summary: Users UpdateProfile
      description: "\n     Users UpdateProfile "
      operationId: users-updateprofile
      parameters:
      - in: query
        name: about
        type: string
      - in: query
        name: location
        description: Defaults to                          Maximum length of 255
        type: string
      - in: query
        name: name
        description: Defaults to                          Minimum length of 2 Maximum
          length of 30
        type: string
      - in: query
        name: url
        description: Defaults to                          URL (defined by RFC 3986)
          Maximum length of 200
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - users
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---