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

        /forums/update.json
  : post:
      summary: Forums Update
      description: "\n     Forums Update "
      operationId: forums-update
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