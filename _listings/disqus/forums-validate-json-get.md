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

        /forums/validate.json
  : get:
      summary: Forums Validate
      description: "\n     Forums Validate "
      operationId: forums-validate
      parameters:
      - in: query
        name: adsPositionBottomEnabled
        description: Defaults to null
        type: string
      - in: query
        name: adsPositionInthreadEnabled
        description: Defaults to null
        type: string
      - in: query
        name: adsPositionTopEnabled
        description: Defaults to null
        type: string
      - in: query
        name: adsProductDisplayEnabled
        description: Defaults to null
        type: string
      - in: query
        name: adsProductLinksEnabled
        description: Defaults to null
        type: string
      - in: query
        name: adsProductStoriesEnabled
        description: Defaults to null
        type: string
      - in: query
        name: adsProductVideoEnabled
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name) You must be a moderator
          on the selected forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - forums
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