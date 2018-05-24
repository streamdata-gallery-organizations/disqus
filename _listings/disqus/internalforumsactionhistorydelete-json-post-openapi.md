---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Internal Forums ActionHistory Delete
  description: Internal Forums ActionHistory Delete
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
      x-api-path-slug: aetdismiss-json-post
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
      x-api-path-slug: aetexport-json-post
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
      x-api-path-slug: aetpendingexportinfo-json-get
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
      x-api-path-slug: aetsubscribe-json-post
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
      x-api-path-slug: blacklistsbackfillcounters-json-post
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
      x-api-path-slug: blacklistslist-json-get
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
      x-api-path-slug: blacklistsremove-json-post
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
      x-api-path-slug: categoriesdetails-json-get
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
      x-api-path-slug: categorieslist-json-get
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
      x-api-path-slug: categorieslistposts-json-get
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
      x-api-path-slug: categorieslistthreads-json-get
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
      x-api-path-slug: forumcategorieslist-json-get
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
      x-api-path-slug: forumscreate-json-post
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
      x-api-path-slug: forumsdetails-json-get
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
      x-api-path-slug: forumsdisableads-json-post
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
      x-api-path-slug: forumsfixfaviconsforclassifiedforums-json-get
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
      x-api-path-slug: forumsfollow-json-post
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
      x-api-path-slug: forumsgenerateinterestingcontent-json-get
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
      x-api-path-slug: forumsinterestingforums-json-get
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
      x-api-path-slug: forumslistcategories-json-get
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
      x-api-path-slug: forumslistfollowers-json-get
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
      x-api-path-slug: forumslistmoderators-json-get
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
      x-api-path-slug: forumslistmostactiveusers-json-get
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
  /forums/listMostLikedUsers.json:
    get:
      summary: Forums ListMostLikedUsers
      description: Forums ListMostLikedUsers
      operationId: forums-listmostlikedusers
      x-api-path-slug: forumslistmostlikedusers-json-get
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
  /forums/listPosts.json:
    get:
      summary: Forums ListPosts
      description: Forums ListPosts
      operationId: forums-listposts
      x-api-path-slug: forumslistposts-json-get
      parameters:
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
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: include
        description: 'Defaults to [  approved]                         Choices: unapproved,
          approved, spam, deleted, flagged, highlighted'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum number of posts
          to return
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
      - Lists
  /forums/listThreads.json:
    get:
      summary: Forums ListThreads
      description: Forums ListThreads
      operationId: forums-listthreads
      x-api-path-slug: forumslistthreads-json-get
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
        name: include
        description: 'Defaults to [  open,  closed]                         Choices:
          open, closed, killed'
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
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID You may pass us the &#39;ident&#39; query type instead of an ID by including
          &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
      - Lists
  /forums/listUserModerationHistory.json:
    get:
      summary: Forums ListUserModerationHistory
      description: Forums ListUserModerationHistory
      operationId: forums-listusermoderationhistory
      x-api-path-slug: forumslistusermoderationhistory-json-get
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
        description: Defaults to 20
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
      - Comments
      - Forums
      - Lists
  /forums/listUsers.json:
    get:
      summary: Forums ListUsers
      description: Forums ListUsers
      operationId: forums-listusers
      x-api-path-slug: forumslistusers-json-get
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
      - Forums
      - Lists
      - Users
  /forums/removeDefaultAvatar.json:
    post:
      summary: Forums RemoveDefaultAvatar
      description: Forums RemoveDefaultAvatar
      operationId: forums-removedefaultavatar
      x-api-path-slug: forumsremovedefaultavatar-json-post
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
  /forums/removeModerator.json:
    post:
      summary: Forums RemoveModerator
      description: Forums RemoveModerator
      operationId: forums-removemoderator
      x-api-path-slug: forumsremovemoderator-json-post
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
      - Comments
      - Forums
  /forums/unfollow.json:
    post:
      summary: Forums Unfollow
      description: Forums Unfollow
      operationId: forums-unfollow
      x-api-path-slug: forumsunfollow-json-post
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
  /forums/update.json:
    post:
      summary: Forums Update
      description: Forums Update
      operationId: forums-update
      x-api-path-slug: forumsupdate-json-post
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
        name: adultContent
        description: Defaults to null
        type: string
      - in: query
        name: aetBannerConfirmation
        description: Defaults to null
        type: string
      - in: query
        name: aetBannerDescription
        description: Defaults to null
        type: string
      - in: query
        name: aetBannerEnabled
        description: Defaults to null
        type: string
      - in: query
        name: aetBannerTitle
        description: Defaults to null
        type: string
      - in: query
        name: allowAnonPost
        description: Defaults to null
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
        name: colorScheme
        description: 'Defaults to null                         Choices: auto, dark,
          light'
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
        name: commentsLinkMultiple
        description: Defaults to null                         Maximum length of 50
        type: string
      - in: query
        name: commentsLinkOne
        description: Defaults to null                         Maximum length of 50
        type: string
      - in: query
        name: commentsLinkZero
        description: Defaults to null                         Maximum length of 50
        type: string
      - in: query
        name: daysThreadAlive
        description: Defaults to null                         Maximum value of 10000
        type: string
      - in: query
        name: description
        description: Defaults to null                         Maximum length of 300
        type: string
      - in: query
        name: disableDisqusBranding
        description: Defaults to null
        type: string
      - in: query
        name: disableThirdPartyTrackers
        description: Defaults to null
        type: string
      - in: query
        name: flaggingEnabled
        description: Defaults to null
        type: string
      - in: query
        name: flaggingNotifications
        description: Defaults to null
        type: string
      - in: query
        name: flagThreshold
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name) You must be a moderator
          on the selected forum
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
        name: installCompleted
        description: Defaults to null
        type: string
      - in: query
        name: linkAffiliationEnabled
        description: Defaults to null
        type: string
      - in: query
        name: mediaembedEnabled
        description: Defaults to null
        type: string
      - in: query
        name: moderatorBadgeText
        description: Defaults to null                         Maximum length of 50
        type: string
      - in: query
        name: name
        description: Defaults to null
        type: string
      - in: query
        name: organicDiscoveryEnabled
        description: Defaults to null
        type: string
      - in: query
        name: shouldError
        description: Defaults to false
        type: string
      - in: query
        name: sort
        description: 'Defaults to null                         Valid values are: 1:
          OLDEST 2: NEWEST 4: HOT'
        type: string
      - in: query
        name: translationLanguage
        description: Defaults to null                         Translation Language
        type: string
      - in: query
        name: twitterName
        description: Defaults to null                         Maximum length of 255
        type: string
      - in: query
        name: typeface
        description: 'Defaults to null                         Choices: auto, serif,
          sans-serif'
        type: string
      - in: query
        name: unapproveLinks
        description: Defaults to null
        type: string
      - in: query
        name: unapproveReputationLevel
        description: 'Defaults to null                         Valid values are: 1:
          LOW1 2: LOW2 3: AVERAGE 4: HIGH'
        type: string
      - in: query
        name: validateAllPosts
        description: Defaults to null
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
  /forums/updateDefaultAvatar.json:
    post:
      summary: Forums UpdateDefaultAvatar
      description: Forums UpdateDefaultAvatar
      operationId: forums-updatedefaultavatar
      x-api-path-slug: forumsupdatedefaultavatar-json-post
      parameters:
      - in: query
        name: avatar_file
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
      - Comments
      - Forums
  /forums/validate.json:
    get:
      summary: Forums Validate
      description: Forums Validate
      operationId: forums-validate
      x-api-path-slug: forumsvalidate-json-get
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
      - Comments
      - Forums
  /imports/list.json:
    get:
      summary: Imports List
      description: Imports List
      operationId: imports-list
      x-api-path-slug: importslist-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Import
      - Lists
  /internal/forums/actionHistory/create.json:
    post:
      summary: Internal Forums ActionHistory Create
      description: Internal Forums ActionHistory Create
      operationId: internal-forums-actionhistory-create
      x-api-path-slug: internalforumsactionhistorycreate-json-post
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
      - Comments
      - Forums
  /internal/forums/actionHistory/delete.json:
    post:
      summary: Internal Forums ActionHistory Delete
      description: Internal Forums ActionHistory Delete
      operationId: internal-forums-actionhistory-delete
      x-api-path-slug: internalforumsactionhistorydelete-json-post
      parameters:
      - in: query
        name: log
        description: Looks up an action history row by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
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