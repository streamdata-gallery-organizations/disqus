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

        /forums/removeModerator.json
  : post:
      summary: Forums RemoveModerator
      description: "\n     Forums RemoveModerator "
      operationId: forums-removemoderator
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: moderator
        description: Defaults to null                         Looks up a moderator,
          either by ID or forum id and user id
        type: string
      - in: query
        name: user
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
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