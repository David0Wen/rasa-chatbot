## happy path
* request_weather
    - weather_form
    - form{"name": "weather_form"}
    - form{"name": null}
    
## happy path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
    - form{"name": null}
* thanks
    - utter_noworries

## unhappy path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* chitchat
    - utter_chitchat
    - weather_form
    - form{"name": null}
* thanks
    - utter_noworries

## very unhappy path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* chitchat
    - utter_chitchat
    - weather_form
* chitchat
    - utter_chitchat
    - weather_form
* chitchat
    - utter_chitchat
    - weather_form
    - form{"name": null}
* thanks
    - utter_noworries

## stop but continue path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* stop
    - utter_ask_continue
* affirm
    - weather_form
    - form{"name": null}
* thanks
    - utter_noworries

## stop and really stop path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* stop
    - utter_ask_continue
* deny
    - action_deactivate_form
    - form{"name": null}

## chitchat stop but continue path
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* chitchat
    - utter_chitchat
    - weather_form
* stop
    - utter_ask_continue
* affirm
    - weather_form
    - form{"name": null}
* thanks
    - utter_noworries

## stop but continue and chitchat path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* stop
    - utter_ask_continue
* affirm
    - weather_form
* chitchat
    - utter_chitchat
    - weather_form
    - form{"name": null}
* thanks
    - utter_noworries

## chitchat stop but continue and chitchat path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* chitchat
    - utter_chitchat
    - weather_form
* stop
    - utter_ask_continue
* affirm
    - weather_form
* chitchat
    - utter_chitchat
    - weather_form
    - form{"name": null}
* thanks
    - utter_noworries

## chitchat, stop and really stop path
* greet
    - utter_answer_greet
* request_weather
    - weather_form
    - form{"name": "weather_form"}
* chitchat
    - utter_chitchat
    - weather_form
* stop
    - utter_ask_continue
* deny
    - action_deactivate_form
    - form{"name": null}
        
## interactive_story_1
## ?????? + ?????? + ?????? + ??????
* request_weather
    - weather_form
    - form{"name": "weather_form"}
    - slot{"requested_slot": "date_time"}
* form: inform{"date_time": "??????"}
    - form: weather_form
    - slot{"date_time": "??????"}
    - slot{"requested_slot": "address"}
* form: inform{"address": "??????"}
    - form: weather_form
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "??????"} OR request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks

## interactive_story_1
## ?????? + ?????? + ?????? + ??????
* request_weather
    - weather_form
    - form{"name": "weather_form"}
    - slot{"requested_slot": "date_time"}
* form: inform{"date_time": "??????"}
    - form: weather_form
    - slot{"date_time": "??????"}
    - slot{"requested_slot": "address"}
* form: inform{"address": "??????"}
    - form: weather_form
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"address": "??????"} OR request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* affirm
    - utter_answer_affirm

## interactive_story_2
## ??????/??????/?????? + ??????
* request_weather{"date_time": "??????", "address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"address": "??????"} OR request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks

## interactive_story_3
## ??????/??????/?????? + ??????
* request_weather{"address": "??????", "date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "?????????"} OR request_weather{"date_time": "?????????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "?????????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks

## interactive_story_2
## ??????/??????/?????? + ?????? + ??????
* request_weather{"date_time": "??????", "address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"address": "??????"} OR request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "??????"} OR request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* affirm
    - utter_answer_affirm

## interactive_story_3
## ??????/??????/?????? + ?????? + ??????
* request_weather{"date_time": "??????", "address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"address": "??????"} OR request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"address": "??????"} OR request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks

## interactive_story_4
## ??????/??????/?????? + ?????? + ??????
* request_weather{"date_time": "??????", "address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "??????"} OR request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "?????????"} OR request_weather{"date_time": "?????????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "?????????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* affirm
    - utter_answer_affirm

## interactive_story_5
## ??????/??????/?????? + ?????? + ??????
* request_weather{"date_time": "??????", "address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "??????"} OR request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"address": "??????"} OR request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks

## interactive_story_4
## ??????/?????? + ?????? + ??????
* request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"requested_slot": "address"}
* form: inform{"address": "??????"}
    - form: weather_form
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "??????"} OR request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks

## interactive_story_5
## ??????/?????? + ?????? + ??????
* request_weather{"address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"address": "??????"}
    - slot{"requested_slot": "date_time"}
* form: inform{"date_time": "??????"}
    - form: weather_form
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* inform{"date_time": "??????"} OR request_weather{"date_time": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - slot{"date_time": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks
    
## interactive_story_1
## ??????/??????/?????? + chit + chit(restart)+????????????
* request_weather{"date_time": "??????", "address": "??????"}
    - weather_form
    - form{"name": "weather_form"}
    - slot{"date_time": "??????"}
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* chitchat
    - utter_chitchat
* chitchat
    - utter_chitchat
    - action_restart
* request_weather
    - weather_form
    - form{"name": "weather_form"}
    - slot{"requested_slot": "date_time"}
* form: inform{"date_time": "??????"}
    - form: weather_form
    - slot{"date_time": "??????"}
    - slot{"requested_slot": "address"}
* form: inform{"address": "??????"}
    - form: weather_form
    - slot{"address": "??????"}
    - form{"name": null}
    - slot{"requested_slot": null}
* thanks
    - utter_answer_thanks