---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Forums ListMostActiveUsers
  description: Forums ListMostActiveUsers
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
  /aet/subscribe.json:
    post:
      summary: Aet Subscribe
      description: Aet Subscribe
      operationId: aet-subscribe
      x-api-path-slug: aetsubscribejson-post
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
  /blacklists/backfillCounters.json:
    post:
      summary: Blacklists BackfillCounters
      description: Blacklists BackfillCounters
      operationId: blacklists-backfillcounters
      x-api-path-slug: blacklistsbackfillcountersjson-post
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Black Lists
  /blacklists/list.json:
    get:
      summary: Blacklists List
      description: Blacklists List
      operationId: blacklists-list
      x-api-path-slug: blacklistslistjson-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: query
        description: Defaults to null
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      - in: query
        name: type
        description: 'Defaults to null                         Choices: domain, word,
          ip, user, thread_slug, email'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Black Lists
  /blacklists/remove.json:
    post:
      summary: Blacklists Remove
      description: Blacklists Remove
      operationId: blacklists-remove
      x-api-path-slug: blacklistsremovejson-post
      parameters:
      - in: query
        name: domain
        description: Defaults to []                         Domain Name
        type: string
      - in: query
        name: email
        description: Defaults to []                         Email address (defined
          by RFC 5322)
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: ip
        description: Defaults to []                         IP address in CIDR notation
        type: string
      - in: query
        name: user
        description: Defaults to []                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      - in: query
        name: word
        description: Defaults to []                         Maximum length of 200
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Black Lists
  /categories/details.json:
    get:
      summary: Categories Details
      description: Categories Details
      operationId: categories-details
      x-api-path-slug: categoriesdetailsjson-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /categories/list.json:
    get:
      summary: Categories List
      description: Categories List
      operationId: categories-list
      x-api-path-slug: categorieslistjson-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /categories/listPosts.json:
    get:
      summary: Categories ListPosts
      description: Categories ListPosts
      operationId: categories-listposts
      x-api-path-slug: categorieslistpostsjson-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: filters
        description: 'Defaults to []                         Valid values are: 1:
          Is_Anonymous 2: Has_Link 3: Has_Low_Rep_Author 4: Has_Bad_Word 5: Is_Flagged
          6: No_Issue 7: Is_Toxic'
        type: string
      - in: query
        name: include
        description: 'Defaults to [  approved]                         Choices: unapproved,
          approved, spam, deleted, flagged, highlighted'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: query
        description: Defaults to null
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /categories/listThreads.json:
    get:
      summary: Categories ListThreads
      description: Categories ListThreads
      operationId: categories-listthreads
      x-api-path-slug: categorieslistthreadsjson-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /forumCategories/list.json:
    get:
      summary: ForumCategories List
      description: ForumCategories List
      operationId: forumcategories-list
      x-api-path-slug: forumcategorieslistjson-get
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
      - Forums
  /forums/create.json:
    post:
      summary: Forums Create
      description: Forums Create
      operationId: forums-create
      x-api-path-slug: forumscreatejson-post
      parameters:
      - in: query
        name: adultContent
        description: Defaults to false
        type: string
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: followsForum,
          forumCanDisableAds, forumForumCategory, counters, forumDaysAlive, forumFeatures,
          forumIntegration, forumNewPolicy, forumPermissions'
        type: string
      - in: query
        name: category
        description: 'Defaults to null                         Choices: Tech, Living,
          Style, Business, Entertainment, Celebrity, Sports, Culture, Games, News'
        type: string
      - in: query
        name: commentPolicyLink
        description: Defaults to null                         URL (defined by RFC
          3986)
        type: string
      - in: query
        name: commentPolicyText
        description: Defaults to null
        type: string
      - in: query
        name: description
        description: Defaults to null                         Maximum length of 300
        type: string
      - in: query
        name: forumCategory
        description: Defaults to null                         Looks up a forum category
          by ID
        type: string
      - in: query
        name: guidelines
        description: Defaults to null
        type: string
      - in: query
        name: language
        description: Defaults to en                         Translation Language
        type: string
      - in: query
        name: name
        type: string
      - in: query
        name: short_name
        type: string
      - in: query
        name: website
        description: Defaults to null                         URL (defined by RFC
          3986)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/details.json:
    get:
      summary: Forums Details
      description: Forums Details
      operationId: forums-details
      x-api-path-slug: forumsdetailsjson-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: followsForum,
          forumCanDisableAds, forumForumCategory, counters, forumDaysAlive, forumFeatures,
          forumIntegration, forumNewPolicy, forumPermissions'
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/disableAds.json:
    post:
      summary: Forums DisableAds
      description: Forums DisableAds
      operationId: forums-disableads
      x-api-path-slug: forumsdisableadsjson-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name) You must be a moderator
          on the selected forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
      - Advertising
  /forums/fixFavIconsForClassifiedForums.json:
    get:
      summary: Forums FixFavIconsForClassifiedForums
      description: Forums FixFavIconsForClassifiedForums
      operationId: forums-fixfaviconsforclassifiedforums
      x-api-path-slug: forumsfixfaviconsforclassifiedforumsjson-get
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/follow.json:
    post:
      summary: Forums Follow
      description: Forums Follow
      operationId: forums-follow
      x-api-path-slug: forumsfollowjson-post
      parameters:
      - in: query
        name: target
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/generateInterestingContent.json:
    get:
      summary: Forums GenerateInterestingContent
      description: Forums GenerateInterestingContent
      operationId: forums-generateinterestingcontent
      x-api-path-slug: forumsgenerateinterestingcontentjson-get
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/interestingForums.json:
    get:
      summary: Forums InterestingForums
      description: Forums InterestingForums
      operationId: forums-interestingforums
      x-api-path-slug: forumsinterestingforumsjson-get
      parameters:
      - in: query
        name: limit
        description: Defaults to 5                         Maximum value of 100
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/listCategories.json:
    get:
      summary: Forums ListCategories
      description: Forums ListCategories
      operationId: forums-listcategories
      x-api-path-slug: forumslistcategoriesjson-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Lists
      - Categories
  /forums/listFollowers.json:
    get:
      summary: Forums ListFollowers
      description: Forums ListFollowers
      operationId: forums-listfollowers
      x-api-path-slug: forumslistfollowersjson-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Lists
  /forums/listModerators.json:
    get:
      summary: Forums ListModerators
      description: Forums ListModerators
      operationId: forums-listmoderators
      x-api-path-slug: forumslistmoderatorsjson-get
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
      - Lists
  /forums/listMostActiveUsers.json:
    get:
      summary: Forums ListMostActiveUsers
      description: Forums ListMostActiveUsers
      operationId: forums-listmostactiveusers
      x-api-path-slug: forumslistmostactiveusersjson-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: desc'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Lists
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