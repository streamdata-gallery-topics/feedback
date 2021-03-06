swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/feedbacks/comment:
    post:
      summary: Create a feedback comment
      description: Creates a feedback comment.
      operationId: postRestFeedbacksComment
      x-api-path-slug: restfeedbackscomment-post
      parameters:
      - in: query
        name: commentRelationTargetId
        description: The ID of the comments target
      - in: query
        name: commentRelationTargetTypeId
        description: The type ID of the comments target
      - in: query
        name: message
        description: Feedback comment message
      responses:
        200:
          description: OK
      tags:
      - Feedback
      - Comment
  /rest/feedbacks/comment/{commentId}:
    delete:
      summary: Delete a feedback comment
      description: Deletes a feedback comment. The ID of the feedback comment must
        be specified.
      operationId: deleteRestFeedbacksCommentComment
      x-api-path-slug: restfeedbackscommentcommentid-delete
      parameters:
      - in: path
        name: commentId
      - in: query
        name: feedbackCommentId
        description: The ID of the feedback comment
      responses:
        200:
          description: OK
      tags:
      - Feedback
      - Comment
    get:
      summary: Get a feedback comment
      description: Gets a feedback comment. The ID of the feedback comment must be
        specified.
      operationId: getRestFeedbacksCommentComment
      x-api-path-slug: restfeedbackscommentcommentid-get
      parameters:
      - in: path
        name: commentId
      - in: query
        name: feedbackCommentId
        description: The ID of the feedback comment
      responses:
        200:
          description: OK
      tags:
      - Feedback
      - Comment
  /rest/feedbacks/comments:
    get:
      summary: List feedback comments
      description: Lists feedback comments.
      operationId: getRestFeedbacksComments
      x-api-path-slug: restfeedbackscomments-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Feedback
      - Comments
  /rest/feedbacks/feedback:
    post:
      summary: Create a feedback
      description: Creates a feedback.
      operationId: postRestFeedbacksFeedback
      x-api-path-slug: restfeedbacksfeedback-post
      parameters:
      - in: query
        name: feedbackRelationSourceTypeId
        description: The type ID of the feedbacks source
      - in: query
        name: feedbackRelationTargetId
        description: The ID of the feedbacks target
      - in: query
        name: feedbackRelationTargetTypeId
        description: The type ID of the feedbacks target
      - in: query
        name: title
        description: Feedback title
      responses:
        200:
          description: OK
      tags:
      - Feedback
  /rest/feedbacks/feedback/replies/{feedbackId}:
    get:
      summary: List feedback replies
      description: Lists feedback replies. The ID of the feedback must be specified.
      operationId: getRestFeedbacksFeedbackRepliesFeedback
      x-api-path-slug: restfeedbacksfeedbackrepliesfeedbackid-get
      parameters:
      - in: path
        name: feedbackId
      responses:
        200:
          description: OK
      tags:
      - List
      - Feedback
      - Replies
  /rest/feedbacks/feedback/{feedbackId}:
    delete:
      summary: Delete a feedback
      description: Deletes a feedback. The ID of the feedback must be specified.
      operationId: deleteRestFeedbacksFeedbackFeedback
      x-api-path-slug: restfeedbacksfeedbackfeedbackid-delete
      parameters:
      - in: path
        name: feedbackId
      responses:
        200:
          description: OK
      tags:
      - Feedback
    get:
      summary: Get a feedback
      description: Gets a feedback. The ID of the feedback must be specified.
      operationId: getRestFeedbacksFeedbackFeedback
      x-api-path-slug: restfeedbacksfeedbackfeedbackid-get
      parameters:
      - in: path
        name: feedbackId
      responses:
        200:
          description: OK
      tags:
      - Feedback
    put:
      summary: Update a feedback
      description: Updates a feedback. The ID of the feedback must be specified.
      operationId: putRestFeedbacksFeedbackFeedback
      x-api-path-slug: restfeedbacksfeedbackfeedbackid-put
      parameters:
      - in: path
        name: feedbackId
      responses:
        200:
          description: OK
      tags:
      - Feedback
  /rest/feedbacks/rating:
    post:
      summary: Create a feedback rating
      description: Creates a feedback rating.
      operationId: postRestFeedbacksRating
      x-api-path-slug: restfeedbacksrating-post
      parameters:
      - in: query
        name: ratingRelationTargetId
        description: The ID of the ratings target
      - in: query
        name: ratingRelationTargetTypeId
        description: The type ID of the ratings target
      - in: query
        name: ratingValue
        description: The feedbacks comment message
      responses:
        200:
          description: OK
      tags:
      - Feedback
      - Rating
  /rest/feedbacks/rating/{ratingId}:
    delete:
      summary: Delete a feedback rating
      description: Deletes a feedback rating. The ID of the feedback rating must be
        specified.
      operationId: deleteRestFeedbacksRatingRating
      x-api-path-slug: restfeedbacksratingratingid-delete
      parameters:
      - in: query
        name: feedbackRatingId
        description: The ID of the feedback rating
      - in: path
        name: ratingId
      responses:
        200:
          description: OK
      tags:
      - Feedback
      - Rating
    get:
      summary: Get a feedback rating
      description: Gets a feedback rating. The ID of the feedback rating must be specified.
      operationId: getRestFeedbacksRatingRating
      x-api-path-slug: restfeedbacksratingratingid-get
      parameters:
      - in: query
        name: feedbackRatingId
        description: The ID of the feedback rating
      - in: path
        name: ratingId
      responses:
        200:
          description: OK
      tags:
      - Feedback
      - Rating
  /rest/feedbacks/ratings:
    get:
      summary: List feedback ratings
      description: Lists feedback ratings.
      operationId: getRestFeedbacksRatings
      x-api-path-slug: restfeedbacksratings-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Feedback
      - Ratings
  /rest/feedbacks/delete_feedbacks/{feedbackIds}:
    delete:
      summary: Delete multiple feedbacks
      description: Deletes multiple feedbacks. A list with IDs of feedbacks must be
        specified.
      operationId: deleteRestFeedbacksDeleteFeedbacksFeedbacks
      x-api-path-slug: restfeedbacksdelete-feedbacksfeedbackids-delete
      parameters:
      - in: path
        name: feedbackIds
      responses:
        200:
          description: OK
      tags:
      - Multiple
      - Feedbacks
  /rest/feedbacks/feedbacks:
    get:
      summary: List feedbacks
      description: Lists feedbacks. The reference type and the reference value must
        be specified (e.g. the reference type is 'order' and the reference value is
        the ID of the order).
      operationId: getRestFeedbacksFeedbacks
      x-api-path-slug: restfeedbacksfeedbacks-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Feedbacks
  /rest/feedbacks/feedbacks_visibility:
    put:
      summary: Update the visibility of multiple feedbacks
      description: Updates the visibility of multiple feedbacks. A list with IDs of
        feedbacks must be specified.
      operationId: putRestFeedbacksFeedbacksVisibility
      x-api-path-slug: restfeedbacksfeedbacks-visibility-put
      parameters:
      - in: query
        name: feedbackIds
        description: The list of feedback IDs, separated by commas
      - in: query
        name: isVisible
        description: The visibility value
      responses:
        200:
          description: OK
      tags:
      - Visibility
      - Of
      - Multiple
      - Feedbacks
  /rest/feedbacks/migrate:
    post:
      summary: Migrate legacy feedbacks
      description: Migrate legacy feedbacks.
      operationId: postRestFeedbacksMigrate
      x-api-path-slug: restfeedbacksmigrate-post
      responses:
        200:
          description: OK
      tags:
      - Migrate
      - Legacy
      - Feedbacks