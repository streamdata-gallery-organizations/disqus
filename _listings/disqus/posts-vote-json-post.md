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

        /posts/vote.json
  : post:
      summary: Posts Vote
      description: "\n     Posts Vote "
      operationId: posts-vote
      parameters:
      - in: query
        name: post
        description: Looks up a post by ID
        type: string
      - in: query
        name: vote
        description: 'Choices: -1, 0, 1'
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - posts
      - votes
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