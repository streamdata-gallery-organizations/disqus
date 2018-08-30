---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Users ListActiveForums
  description: Users ListActiveForums
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
  /internal/forums/actionHistory/update.json:
    post:
      summary: Internal Forums ActionHistory Update
      description: Internal Forums ActionHistory Update
      operationId: internal-forums-actionhistory-update
      x-api-path-slug: internalforumsactionhistoryupdate-json-post
      parameters:
      - in: query
        name: action
        description: 'Defaults to null                         Valid values are: 1:
          ApprovePost 2: UnapprovePost 3: SpamPost 4: UnspamPost 5: RestorePost 6:
          RemovePost 7: HighlightPost 8: UnhighlightPost 9: AddBlacklist 10: RemoveBlacklist'
        type: string
      - in: query
        name: dateAdded
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: ip
        description: Defaults to null                         IP address (defined
          by RFC 5322)
        type: string
      - in: query
        name: log
        description: Looks up an action history row by ID
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
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /organizations/listAdmins.json:
    get:
      summary: Organizations ListAdmins
      description: Organizations ListAdmins
      operationId: organizations-listadmins
      x-api-path-slug: organizationslistadmins-json-get
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations
  /organizations/removeAdmin.json:
    post:
      summary: Organizations RemoveAdmin
      description: Organizations RemoveAdmin
      operationId: organizations-removeadmin
      x-api-path-slug: organizationsremoveadmin-json-post
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
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
      - Organizations
  /organizations/setRole.json:
    post:
      summary: Organizations SetRole
      description: Organizations SetRole
      operationId: organizations-setrole
      x-api-path-slug: organizationssetrole-json-post
      parameters:
      - in: query
        name: isAdmin
        description: Defaults to null
        type: string
      - in: query
        name: isModerator
        description: Defaults to null
        type: string
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
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
      - Organizations
  /organizations/saas/currentPlan.json:
    get:
      summary: Organizations Saas CurrentPlan
      description: Organizations Saas CurrentPlan
      operationId: organizations-saas-currentplan
      x-api-path-slug: organizationssaascurrentplan-json-get
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations
  /organizations/saas/removePaymentInfo.json:
    post:
      summary: Organizations Saas RemovePaymentInfo
      description: Organizations Saas RemovePaymentInfo
      operationId: organizations-saas-removepaymentinfo
      x-api-path-slug: organizationssaasremovepaymentinfo-json-post
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations
  /organizations/saas/subscribe.json:
    post:
      summary: Organizations Saas Subscribe
      description: Organizations Saas Subscribe
      operationId: organizations-saas-subscribe
      x-api-path-slug: organizationssaassubscribe-json-post
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      - in: query
        name: plan
        description: Looks up a PricingOption by name
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
      - Organizations
  /organizations/saas/unsubscribe.json:
    post:
      summary: Organizations Saas Unsubscribe
      description: Organizations Saas Unsubscribe
      operationId: organizations-saas-unsubscribe
      x-api-path-slug: organizationssaasunsubscribe-json-post
      parameters:
      - in: query
        name: immediately
        description: Defaults to false
        type: string
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations
  /organizations/saas/updatePaymentInfo.json:
    post:
      summary: Organizations Saas UpdatePaymentInfo
      description: Organizations Saas UpdatePaymentInfo
      operationId: organizations-saas-updatepaymentinfo
      x-api-path-slug: organizationssaasupdatepaymentinfo-json-post
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      - in: query
        name: token
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations
  /posts/create.json:
    post:
      summary: Posts Create
      description: Posts Create
      operationId: posts-create
      x-api-path-slug: postscreate-json-post
      parameters:
      - in: query
        name: author_email
        description: Defaults to null                         Email address (defined
          by RFC 5322)
        type: string
      - in: query
        name: author_name
        description: Defaults to null
        type: string
      - in: query
        name: author_url
        description: Defaults to null                         URL (defined by RFC
          3986)
        type: string
      - in: query
        name: date
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: ip_address
        description: Defaults to null                         IP address (defined
          by RFC 5322)
        type: string
      - in: query
        name: message
        type: string
      - in: query
        name: parent
        description: Defaults to null                         Looks up a post by ID
        type: string
      - in: query
        name: state
        description: 'Defaults to null                         Choices: unapproved,
          approved, spam, killed'
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/details.json:
    get:
      summary: Posts Details
      description: Posts Details
      operationId: posts-details
      x-api-path-slug: postsdetails-json-get
      parameters:
      - in: query
        name: post
        description: Looks up a post by ID
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
      - Posts
  /posts/getContext.json:
    get:
      summary: Posts GetContext
      description: Posts GetContext
      operationId: posts-getcontext
      x-api-path-slug: postsgetcontext-json-get
      parameters:
      - in: query
        name: depth
        description: Defaults to 10                         Minimum value of 1 Maximum
          value of 10
        type: string
      - in: query
        name: post
        description: Looks up a post by ID
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
      - Posts
  /posts/list.json:
    get:
      summary: Posts List
      description: Posts List
      operationId: posts-list
      x-api-path-slug: postslist-json-get
      parameters:
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: end
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: filters
        description: 'Defaults to []                         Valid values are: 1:
          Is_Anonymous 2: Has_Link 3: Has_Low_Rep_Author 4: Has_Bad_Word 5: Is_Flagged
          6: No_Issue 7: Is_Toxic'
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Defaults to all forums
          you moderate
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
        name: offset
        description: 'Defaults to 0                         Deprecated: Please see
          documentation on cursors'
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
      - in: query
        name: sortType
        description: 'Defaults to date                         Choices: date, priority'
        type: string
      - in: query
        name: start
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/listModerationHistory.json:
    get:
      summary: Posts ListModerationHistory
      description: Posts ListModerationHistory
      operationId: posts-listmoderationhistory
      x-api-path-slug: postslistmoderationhistory-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: limit
        description: Defaults to 20
        type: string
      - in: query
        name: post
        description: Looks up a post by ID You must be a moderator on the selected
          post&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/listPopular.json:
    get:
      summary: Posts ListPopular
      description: Posts ListPopular
      operationId: posts-listpopular
      x-api-path-slug: postslistpopular-json-get
      parameters:
      - in: query
        name: category
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Defaults to all forums
          you moderate
        type: string
      - in: query
        name: include
        description: 'Defaults to [  approved]                         Choices: unapproved,
          approved, spam, deleted, flagged, highlighted'
        type: string
      - in: query
        name: interval
        description: 'Defaults to 7d                         Choices: 1h, 6h, 12h,
          1d, 3d, 7d, 30d, 60d, 90d'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: offset
        description: Defaults to 0
        type: string
      - in: query
        name: order
        description: 'Defaults to popular                         Choices: popular,
          best'
        type: string
      - in: query
        name: organization
        description: Defaults to null                         Looks up an organization
          by ID
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
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/listReporters.json:
    get:
      summary: Posts ListReporters
      description: Posts ListReporters
      operationId: posts-listreporters
      x-api-path-slug: postslistreporters-json-get
      parameters:
      - in: query
        name: numberPerPost
        description: Defaults to 1
        type: string
      - in: query
        name: posts
        description: Looks up a post by ID You must be a moderator on the selected
          post&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/remove.json:
    post:
      summary: Posts Remove
      description: Posts Remove
      operationId: posts-remove
      x-api-path-slug: postsremove-json-post
      parameters:
      - in: query
        name: post
        description: Looks up a post by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/report.json:
    post:
      summary: Posts Report
      description: Posts Report
      operationId: posts-report
      x-api-path-slug: postsreport-json-post
      parameters:
      - in: query
        name: post
        description: Looks up a post by ID
        type: string
      - in: query
        name: reason
        description: 'Defaults to null                         Valid values are: 0:
          HARASSMENT 1: SPAM 2: INAPPROPRIATE_CONTENT 3: THREAT 4: IMPERSONATION 5:
          PRIVATE_INFORMATION 6: DISAGREE'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/restore.json:
    post:
      summary: Posts Restore
      description: Posts Restore
      operationId: posts-restore
      x-api-path-slug: postsrestore-json-post
      parameters:
      - in: query
        name: post
        description: Looks up a post by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/spam.json:
    post:
      summary: Posts Spam
      description: Posts Spam
      operationId: posts-spam
      x-api-path-slug: postsspam-json-post
      parameters:
      - in: query
        name: post
        description: Looks up a post by ID You must be a moderator on the selected
          post&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
      - Spam
  /posts/update.json:
    post:
      summary: Posts Update
      description: Posts Update
      operationId: posts-update
      x-api-path-slug: postsupdate-json-post
      parameters:
      - in: query
        name: message
        type: string
      - in: query
        name: post
        description: You must be the author of the post or a moderator on the applicable
          forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Posts
  /posts/vote.json:
    post:
      summary: Posts Vote
      description: Posts Vote
      operationId: posts-vote
      x-api-path-slug: postsvote-json-post
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
      - Comments
      - Posts
      - Votes
  /threads/close.json:
    post:
      summary: Threads Close
      description: Threads Close
      operationId: threads-close
      x-api-path-slug: threadsclose-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You must be a moderator on the selected
          thread&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/create.json:
    post:
      summary: Threads Create
      description: Threads Create
      operationId: threads-create
      x-api-path-slug: threadscreate-json-post
      parameters:
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: date
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: identifier
        description: Defaults to null                         Maximum length of 300
        type: string
      - in: query
        name: message
        description: Defaults to null
        type: string
      - in: query
        name: slug
        description: Defaults to null                         Alpha-numeric slug Maximum
          length of 200
        type: string
      - in: query
        name: title
        type: string
      - in: query
        name: url
        description: Defaults to null                         URL (defined by RFC
          3986) Maximum length of 500
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/details.json:
    get:
      summary: Threads Details
      description: Threads Details
      operationId: threads-details
      x-api-path-slug: threadsdetails-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: topics'
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; or
          &#39;link&#39; query types instead of an ID by including &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/list.json:
    get:
      summary: Threads List
      description: Threads List
      operationId: threads-list
      x-api-path-slug: threadslist-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: topics'
        type: string
      - in: query
        name: author
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
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
      - Threads
  /threads/listHot.json:
    get:
      summary: Threads ListHot
      description: Threads ListHot
      operationId: threads-listhot
      x-api-path-slug: threadslisthot-json-get
      parameters:
      - in: query
        name: author
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
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
        name: include
        description: 'Defaults to [  open,  closed]                         Choices:
          open, closed, killed'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
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
      - Threads
  /threads/listPopular.json:
    get:
      summary: Threads ListPopular
      description: Threads ListPopular
      operationId: threads-listpopular
      x-api-path-slug: threadslistpopular-json-get
      parameters:
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
        name: interval
        description: 'Defaults to 7d                         Choices: 1h, 6h, 12h,
          1d, 3d, 7d, 30d, 90d'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: with_top_post
        description: Defaults to false
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/listPosts.json:
    get:
      summary: Threads ListPosts
      description: Threads ListPosts
      operationId: threads-listposts
      x-api-path-slug: threadslistposts-json-get
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
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
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
      - in: query
        name: thread
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; or
          &#39;link&#39; query types instead of an ID by including &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/listUsersVotedThread.json:
    get:
      summary: Threads ListUsersVotedThread
      description: Threads ListUsersVotedThread
      operationId: threads-listusersvotedthread
      x-api-path-slug: threadslistusersvotedthread-json-get
      parameters:
      - in: query
        name: limit
        description: Defaults to 10                         Maximum value of 100
        type: string
      - in: query
        name: prioritize_followed
        description: Defaults to true                         Prioritize followed
          users who voted on this thread (must be authenticated)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID
        type: string
      - in: query
        name: vote
        description: 'Defaults to 1                         Choices: -1, 0, 1'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/open.json:
    post:
      summary: Threads Open
      description: Threads Open
      operationId: threads-open
      x-api-path-slug: threadsopen-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You must be a moderator on the selected
          thread&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/remove.json:
    post:
      summary: Threads Remove
      description: Threads Remove
      operationId: threads-remove
      x-api-path-slug: threadsremove-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You must be a moderator on the selected
          thread&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/restore.json:
    post:
      summary: Threads Restore
      description: Threads Restore
      operationId: threads-restore
      x-api-path-slug: threadsrestore-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You must be a moderator on the selected
          thread&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/set.json:
    get:
      summary: Threads Set
      description: Threads Set
      operationId: threads-set
      x-api-path-slug: threadsset-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: topics'
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; query
          type instead of an ID by including &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/spam.json:
    post:
      summary: Threads Spam
      description: Threads Spam
      operationId: threads-spam
      x-api-path-slug: threadsspam-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You must be a moderator on the selected
          thread&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
      - Spam
  /threads/subscribe.json:
    post:
      summary: Threads Subscribe
      description: Threads Subscribe
      operationId: threads-subscribe
      x-api-path-slug: threadssubscribe-json-post
      parameters:
      - in: query
        name: thread
        description: Looks up a thread by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/unsubscribe.json:
    post:
      summary: Threads Unsubscribe
      description: Threads Unsubscribe
      operationId: threads-unsubscribe
      x-api-path-slug: threadsunsubscribe-json-post
      parameters:
      - in: query
        name: thread
        description: Looks up a thread by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/update.json:
    post:
      summary: Threads Update
      description: Threads Update
      operationId: threads-update
      x-api-path-slug: threadsupdate-json-post
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
      - Comments
      - Threads
  /threads/vote.json:
    post:
      summary: Threads Vote
      description: Threads Vote
      operationId: threads-vote
      x-api-path-slug: threadsvote-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; or
          &#39;link&#39; query types instead of an ID by including &#39;forum&#39;
        type: string
      - in: query
        name: vote
        description: 'Choices: -1, 0, 1'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
      - Vote
  /forums/trustedDomain/kill.json:
    post:
      summary: Forums TrustedDomain Kill
      description: Forums TrustedDomain Kill
      operationId: forums-trusteddomain-kill
      x-api-path-slug: forumstrusteddomainkill-json-post
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
      - Comments
      - Forums
  /forums/trustedDomain/list.json:
    get:
      summary: Forums TrustedDomain List
      description: Forums TrustedDomain List
      operationId: forums-trusteddomain-list
      x-api-path-slug: forumstrusteddomainlist-json-get
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
  /users/details.json:
    get:
      summary: Users Details
      description: Users Details
      operationId: users-details
      x-api-path-slug: usersdetails-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: userFlaggedUser'
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
      - Users
  /users/follow.json:
    post:
      summary: Users Follow
      description: Users Follow
      operationId: users-follow
      x-api-path-slug: usersfollow-json-post
      parameters:
      - in: query
        name: target
        description: Looks up a user by ID You may look up a user by username using
          the &#39;username&#39; query type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Users
  /users/listActiveForums.json:
    get:
      summary: Users ListActiveForums
      description: Users ListActiveForums
      operationId: users-listactiveforums
      x-api-path-slug: userslistactiveforums-json-get
      parameters:
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
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
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
      - Users
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