
# Questions

## Questions List

> Request:

```shell
curl "https://yoursite.cultivateforecasts.com/api/v1/questions" \
  -H "Authorization: Bearer b95b4f848cd226e55b7a42f6a8e8669350730270f5a91d64b6c70328b0156d75"
```

> Response:

```json
{
  "questions": [
    {
      "id": 5,
      "discover_question_id": 123,
      "name": "question-2",
      "type": "Forecast::Question",
      "site_id": 1,
      "membership_id": 1,
      "ends_at": "2015-09-15T00:21:35.906Z",
      "description": "question-desc-5",
      "published_at": null,
      "starts_at": null,
      "resolved_at": "2015-09-15T00:21:35.906Z",
      "voided_at": null,
      "post_forecast_survey_id": null,
      "predictions_count": 0,
      "comments_count": 0,
      "created_at": "2015-08-04T00:21:35.910Z",
      "updated_at": "2015-08-04T00:21:35.910Z",
      "scoring_start_time": "2015-09-15T00:21:35.906Z",
      "scoring_end_time": "2015-09-15T00:21:35.906Z",
      "state": "resolved",
      "active?": false,
      "resolved?": true,
      "resolution_notes": [
        "This question was resolved based on the ABC data source."
      ],
      "use_ordinal_scoring": false,
      "answers": [
        {
          "created_at": "2015-08-04T00:21:35.918Z",
          "ends_at": "2016-02-04T00:21:35.916Z",
          "id": 11,
          "discover_answer_id": 423,
          "membership_id": 1,
          "name": "answer-name-11",
          "outstanding": 0,
          "positions_count": null,
          "predictions_count": 0,
          "probability": "0.3333",
          "probability_formatted": "33.33%",
          "question_id": 5,
          "refunded_at": null,
          "refunded_by_id": null,
          "resolved_at": "2015-09-15T00:21:35.906Z",
          "resolved_by_id": 12,
          "correctness_known_at": "2015-09-15T00:21:35.906Z",
          "type": null,
          "updated_at": "2015-08-04T00:21:35.918Z"
        },
        {
          "created_at": "2015-08-04T00:21:35.927Z",
          "ends_at": "2016-02-04T00:21:35.925Z",
          "id": 12,
          "discover_answer_id": 424,
          "membership_id": 1,
          "name": "answer-name-12",
          "outstanding": 0,
          "positions_count": null,
          "predictions_count": 0,
          "probability": "0.3333",
          "probability_formatted": "33.33%",
          "question_id": 5,
          "refunded_at": null,
          "refunded_by_id": null,
          "resolved_at": "2015-09-15T00:21:35.906Z",
          "resolved_by_id": 12,
          "correctness_known_at": "2015-09-15T00:21:35.906Z",
          "type": null,
          "updated_at": "2015-08-04T00:21:35.927Z"
        },
        {
          "created_at": "2015-08-04T00:21:35.933Z",
          "ends_at": "2016-02-04T00:21:35.931Z",
          "id": 13,
          "discover_answer_id": 425,
          "membership_id": 1,
          "name": "answer-name-13",
          "outstanding": 0,
          "positions_count": null,
          "predictions_count": 0,
          "probability": "0.3333",
          "probability_formatted": "33.33%",
          "question_id": 5,
          "refunded_at": null,
          "refunded_by_id": null,
          "resolved_at": "2015-09-15T00:21:35.906Z",
          "resolved_by_id": 12,
          "correctness_known_at": "2015-09-15T00:21:35.906Z",
          "type": null,
          "updated_at": "2015-08-04T00:21:35.933Z"
        }
      ],
      "clarifications":[{
        "id":4,
        "question_id":5,
        "content":"clarification-content-1",
        "created_at":"2018-01-15T21:45:32.495Z",
        "updated_at":"2018-01-15T21:45:32.495Z"
      }]
    },
    {
      "id": 6,
      "discover_question_id": 31,
      "name": "binary_question-2",
      "type": "Forecast::Binary::Question",
      "site_id": 1,
      "membership_id": 1,
      "ends_at": "2015-09-15T00:21:35.945Z",
      "description": "question-desc-6",
      "published_at": null,
      "starts_at": null,
      "resolved_at": null,
      "voided_at": null,
      "post_forecast_survey_id": null,
      "predictions_count": 0,
      "comments_count": 0,
      "created_at": "2015-08-04T00:21:35.953Z",
      "updated_at": "2015-08-04T00:21:35.953Z",
      "scoring_start_time": "2015-09-15T00:21:35.906Z",
      "scoring_end_time": null,
      "state": "pending",
      "active?": true,
      "resolved?": false,
      "use_ordinal_scoring": false,
      "answers": [
        {
          "created_at": "2015-08-04T00:21:35.965Z",
          "ends_at": "2016-02-04T00:21:35.962Z",
          "id": 14,
          "discover_answer_id": 429,
          "membership_id": 1,
          "name": "answer-name-14",
          "outstanding": 0,
          "positions_count": null,
          "predictions_count": 0,
          "probability": "0.5",
          "probability_formatted": "50.00%",
          "question_id": 6,
          "refunded_at": null,
          "refunded_by_id": null,
          "resolved_at": null,
          "resolved_by_id": null,
          "correctness_known_at": null,
          "type": "Forecast::Binary::Answer",
          "updated_at": "2015-08-04T00:21:35.965Z"
        }
      ]
    }
  ]
}
```

### HTTP Request

`GET https://yoursite.cultivateforecasts.com/api/v1/questions`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 0 | Pagination page number
ids  | none | A comma separated list of question ID's to return (e.g. "123,124,125")
tags | none | A comma separated list of tags to filter by (e.g. "sports,politics,tech")
challenges | none | A comma separated list of challenge ids to filter by (e.g. "1,5,8"). Will return only questions in those challenges. Operates as a logical AND (ie. if you pass "1,5", it will return only questions that are in both challenges)
filter | none | A filter to apply to the question list. Possible values: `starred`, `featured`. By default, no filter is applied.
status | active | A question status filter to apply to the question list. Possible values: `closed`, `all`. If this value is omitted, only active questions are returned. To include all questions, you should pass `all` for this value.
sort | published_at | Sort order for the questions. Possible values: `published_at`, `ends_at`, `resolved_at`, `prediction_sets_count`
created_before | none | Returns only questions created before the passed date. Date should be in iso8601 format (e.g. 2015-08-23T15:43:11-05:00)
created_after | none | Returns only questions created after the passed date. Date should be in iso8601 format (e.g. 2015-08-23T15:43:11-05:00)
updated_before | none | Returns only questions updated before the passed date. Date should be in iso8601 format (e.g. 2015-08-23T15:43:11-05:00)
updated_after | none | Returns only questions updated after the passed date. Date should be in iso8601 format (e.g. 2015-08-23T15:43:11-05:00)
include_tag_ids | false | Passing "true" for this value will include an array of tag ids for the question.
include_challenge_ids | false | Passing "true" for this value will include an array of challenge ids for the question.

### Question Attributes

Parameter | Type | Description
--------- | ------- | -----------
active | boolean | Whether or not this question is currently active for forecasting
clarifications | array | An array of clarifications issued for the question. Used to clarify things like resolution criteria for the question.
comments_count | integer | The number of comments that have been made in this question  
created_at | datetime | The date & time that this question was created
description | string | The description & background information for the question
discover_question_id | integer | The id of the discover question used to generate/publish this question, if collaborative question generation (Discover) is being used
ends_at | datetime | The date & time that this question stops accepting forecasts
id | integer | The id of the question
membership_id | integer | The id of the membership who created this question
name | string | The question content
post_forecast_survey_id | integer | If a survey is administered after forecasts in this question, the ID of that survey
predictions_count | integer | The number of predictions that have been made in this question
published_at | datetime | The date & time that this question was published
resolution_notes | array | Any notes/information provided by an admin describing the resolution of the question and any data sources used.
resolved | boolean | Whether or not this question has been resolved
resolved_at | datetime | The date & time that this question was resolved
scoring_end_time | datetime | The time at which scoring ends for this question.
scoring_start_time | datetime | The time at which scoring starts for this question.
site_id | integer | The id of the site that this question belongs to
starts_at | datetime | The date & time that this question started accepting forecasts
state | string | The current state of the question. Options enumerated in [question states](#question-states)
type | string | The internal question type (e.g. prediction market, binary prediction market, opinion pool)
updated_at | datetime | The date & time that this question was last updated
use_ordinal_scoring | boolean | Whether or not this question uses ordinal scoring for calculating Brier scores
voided_at | datetime | The date & time that this question was voided. Blank if the question has not been voided. A voided question will not be resolved or scored.

### Answer Attributes

Parameter | Type | Description
--------- | ------- | -----------
id | integer | The id of the answer
discover_answer_id | integer | The id of the discover answer used to generate/publish this question, if collaborative question generation (Discover) is being used
created_at | datetime | The date & time that this answer was created
updated_at | datetime | The date & time that this answer was last updated
ends_at | datetime | The date & time that this answer stops accepting forecasts
membership_id | integer | The id of the membership who created this answer
name | string | The answer content
outstanding | integer | If this question is a prediction market, this represents the number of outstanding shares in this stock
positions_count | integer | The number of positions forecasters have taken in this answer
predictions_count | integer | The number of predictions forecasters have made in this answer
probability | float | The current consensus probability for this answer
probability_formatted | string | The current consensus probability for this answer, formatted as a percentage
question_id | integer | The id of the question that this answer belongs to
refunded_at | datetime | If this question is a prediction market and this stock has been refunded, the date & time the refund occurred
refunded_by_id | integer | The membership_id of the membership who refunded this stock
resolved_at | datetime | The date & time that this answer was resolved
resolved_by_id | integer | The memebership_id of the membership who resolved this answer
correctness_known_at | datetime | The date & time that the correctness of this answer was known. If an administrator sets this value when resolving the answer, all forecasts made after it will be invalidated.
type | string | The internal answer type (e.g. prediction market stock, opinion pool answer)


### Question States

State | Description
----- | -----------
active | Currently open for forecasting
rejected | An admin rejected the suggested question. It won't be published for forecasting.
voided | The question was published for forecasting, but subsequently voided due to unforeseen issues with the question. It will not be scored or resolved.
refunded | Only applicable to prediction market-type questions. Roughly the same as `voided`, but all trades were refunded.
resolved | The question has ended, been judged, and scored (or is in the process of scoring).
pending | An admin created the question, but has not yet published it.
pending_resolution | The question's `ends_at` timestamp has passed, but it has not yet been resolved.



## Questions Creation and Updating

> HTTP Request:

`POST https://yoursite.cultivateforecasts.com/api/v1/questions`
`PATCH https://yoursite.cultivateforecasts.com/api/v1/questions/:id`

> Request body example:

```json
{
  "question": {
    "name": "How many tournaments will Tiger win this year?",
    "description": "This question includes only major tournaments"
    "ends_at": "2017-12-31T23:59:59Z"
    "type": "Forecast::PM::LMSR::ExclusiveMarket"
    "answers_attributes": {
      "1": {
        "name": "0",
        "probability_whole_number": 47.5
      },
      "2": {
        "name": "1-5",
        "probability_whole_number": 22.5
      },
      "3": {
        "name": "6 or more",
        "probability_whole_number": 30
      }
    }
  }
}
```


### Question Parameters

Parameter | Required? | Description
--------- | --------- | -----------
name | Yes | The name of the question
description | Yes | Background information, displays below the question name
links_attributes | No | An array of links to display below the question name. Valid parameters for links are listed below.
starts_at | No | The time at which the question begins accepting forecasts
ends_at | Yes | The time at which the question stops accepting forecasts
type | Yes | Valid question types are listed below -- note that some question types are disabled on some sites
intro | No | An introduction that appears before the question name. eg "Sponsor XYZ presents:"
use_ordinal_scoring | No | An optional scoring setting for questions with sequential answers
rolling_range_count | No | For rolling questions, the number of answers active at a given time
rolling_time_length | No | For rolling questions, the number of time units allotted to each answer (eg 2 for two weeks, 4 for four years)
rolling_time_unit | No | For rolling questions, the unit of time for each answer. Options: "day", "week", "month", "year"
roll_percentage | No | For rolling questions, the percentage of the probability assigned to the last bucket (eg 2020 or later) that will be transfered to the newly created bucket (2021 or later). The remainder will be assigned to the second last bucket (2020)
tag_list | No | An array containing the names of tags to be assigned to this question
challenge_ids | No | An array containing ids of challenges to be assigned to this question
answers_attributes | Yes | A hash of answer objects that are part of this question. Valid parameters for answers are listed below.
suspended | No | If selected, the question is suspended and does not accept new forecasts

### Answer Parameters

Parameter | Required? | Description
--------- | --------- | -----------
name | Yes | The name of the answer
probability_whole_number | Yes | The starting probability of the answer
sort_order | No | The order in which this answer is displayed
id | No | The unique id of the answer--use only for updating
discover_answer_id | No | For questions created via Discover, the id of the Discover answer that corresponds to this answer
_destroy | No | Set to "true" to destroy this answer

### Link Parameters

Parameter | Description
--------- | -----------
id | The unique id of the link--use only for updating
url | The url address of this link
description | The text that displays for this link
_destroy | Set to "true" to destroy this link

### Question Types

Question Type | Description
------------- | -----------
"Forecast::Question" | A multi-answer prediction pool
"Forecast::Binary::Question" | A prediction pool with only one answer (eg Yes/No)
"Forecast::RollingQuestion" | A rolling prediction pool, with new answers appearing over time
"Forecast::PM::LMSR::ExclusiveMarket" | A multi-answer prediction market with one correct answer
"Forecast::PM::LMSR::NonExclusiveMarket" | A multi-answer prediction market that allows multiple correct answers
"Forecast::PM::LMSR::BinaryMarket" | A prediction market with only one answer
"Forecast::PM::LMSR::RollingMarket" | A rolling prediction market, with new answers appearing over time
