## fallback
- utter_default

## greeting path 1
* greet
* greet
- utter_greet

## fine path 1
* fine_normal
- utter_help

## fine path 2
* fine_ask
- utter_reply

## news path
* news
- utter_ofc
- action_get_news

## thanks path 1
* thanks
- utter_anything_else

## bye path 1
* bye
- utter_bye

## Covid-19 path1

    - utter_greet
    - slot{"category":"world"}
* greet
    - utter_help
    - slot{"category":"covid-19"}
* news{"category":"covid-19"}
    - utter_ofc
    - action_get_news

## Normal convo

* greet
    - utter_greet
* fine_normal
    - utter_help
    - slot{"category":"world"}
* news{"category":"world"}
    - action_get_news
    - utter_anything_else
* thanks
    - utter_bye

## Sample flow chart

    - utter_wrong_name
* greet
    - utter_wyd
* news
    - utter_out_of_scope
    - slot{"category":"world"}
* news{"category":"world"}
    - utter_ofc
    - action_get_news

## New Story

* greet
    - utter_greet

## New Story

* greet
    - utter_greet
* fine_ask
    - utter_reply
    - slot{"category":"covid-19"}
* news{"category":"covid-19"}
    - action_get_news
    - utter_anything_else
* thanks
    - utter_bye

## New Story

    - utter_greet
    - slot{"category":"world"}
* greet
    - utter_anything_else
* thanks
    - utter_bye

## New Story

    - utter_greet
    - slot{"category":"sports"}
* greet
    - utter_out_of_scope
* news
    - utter_out_of_scope

## New Story

* greet
    - utter_greet

## New Story

* greet
    - utter_greet

## New Story

* greet
    - utter_greet
* fine_ask
    - utter_reply
* fine_ask
    - utter_wyd
    - slot{"category":"sports"}
* news{"category":"sports"}
    - utter_ofc
    - action_get_news
* thanks
    - utter_anything_else
* bye
    - utter_bye
* bye
    - utter_bye

## New Story

* fine_ask
    - utter_wyd

## New Story

* wyd_question
    - utter_wyd
