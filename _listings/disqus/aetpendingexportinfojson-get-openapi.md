---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Aet PendingExportInfo
  description: Aet PendingExportInfo
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
  /aet/dismiss.json:
    post:
      summary: Aet Dismiss
      description: Aet Dismiss
      operationId: aet-dismiss
      x-api-path-slug: aetdismissjson-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
  /aet/export.json:
    post:
      summary: Aet Export
      description: Aet Export
      operationId: aet-export
      x-api-path-slug: aetexportjson-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name) You must be a moderator
          on the selected forum
        type: string
      - in: query
        name: full
        description: Defaults to false                         If true, export all
          emails collected so far
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
  /aet/pendingExportInfo.json:
    get:
      summary: Aet PendingExportInfo
      description: Aet PendingExportInfo
      operationId: aet-pendingexportinfo
      x-api-path-slug: aetpendingexportinfojson-get
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Export
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