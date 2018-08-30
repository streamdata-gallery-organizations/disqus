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

        /threads/update.json
  : post:
      summary: Threads Update
      description: "\n     Threads Update "
      operationId: threads-update
      parameters:
      - in: query
        name: author
        description: Defaults to null                         You must be a moderator
          on the applicable forum to change a thread author
        type: string
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: identifier
        description: Defaults to null                         To update a specific
          identifier, provide &#39;old_identifier&#39;
        type: string
      - in: query
        name: message
        description: Defaults to null
        type: string
      - in: query
        name: old_identifier
        description: Defaults to null                         Only valid if &#39;identifier&#39;
          is provided
        type: string
      - in: query
        name: slug
        description: Defaults to null                         Alpha-numeric slug Maximum
          length of 200
        type: string
      - in: query
        name: thread
        description: You must be the author of the post or a moderator on the applicable
          forum
        type: string
      - in: query
        name: title
        description: Defaults to null                         Maximum length of 200
        type: string
      - in: query
        name: url
        description: Defaults to null                         URL (defined by RFC
          3986) Maximum length of 500
        type: string
      - in: query
        name: validateAllPosts
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - threads
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