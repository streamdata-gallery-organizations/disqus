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

        /internal/forums/actionHistory/create.json
  : post:
      summary: Internal Forums ActionHistory Create
      description: "\n     Internal Forums ActionHistory Create "
      operationId: internal-forums-actionhistory-create
      parameters:
      - in: query
        name: action
        description: 'Valid values are: 1: ApprovePost 2: UnapprovePost 3: SpamPost
          4: UnspamPost 5: RestorePost 6: RemovePost 7: HighlightPost 8: UnhighlightPost
          9: AddBlacklist 10: RemoveBlacklist'
        type: string
      - in: query
        name: dateAdded
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: ip
        description: Defaults to null                         IP address (defined
          by RFC 5322)
        type: string
      - in: query
        name: post
        description: Defaults to null                         Looks up a post by ID
        type: string
      - in: query
        name: targetUser
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID
        type: string
      - in: query
        name: user
        description: Looks up a user by ID You may look up a user by username using
          the &#39;username&#39; query type
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