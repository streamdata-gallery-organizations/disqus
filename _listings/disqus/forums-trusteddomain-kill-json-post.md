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

        /forums/trustedDomain/kill.json
  : post:
      summary: Forums TrustedDomain Kill
      description: "\n     Forums TrustedDomain Kill "
      operationId: forums-trusteddomain-kill
      parameters:
      - in: query
        name: domain
        description: Looks up a trusted domain by id, or by domain name if forum provided
          You may pass us the &#39;domain&#39; query type instead of an ID by including
          &#39;forum&#39;
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name) You must be a moderator on the selected forum
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