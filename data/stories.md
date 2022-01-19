## happy path
* greet
   - utter_greet
* mood_great
   - utter_happy

## sad path 1
* greet
   - utter_greet
* mood_unhappy
   - utter_cheer_up
   - utter_did_that_help
* affirm
   - utter_happy

## story: sad path 2
* greet
   - utter_greet
* mood_unhappy
   - utter_cheer_up
   - utter_did_that_help
* deny
   - utter_goodbye

## story: ask diet questions
* ask_eat_healthy
   - utter_diet_info

## story: stress questions
* ask_lower_stress
   - utter_stress_info

## story: ask exercise
* ask_exercise
   - utter_exercise_info

## story: interactive_story_1
* greet
   - utter_greet
* ask_lower_stress
   - utter_stress_info
* ask_eat_healthy
   - utter_diet_info

## story: survey happy path
* greet
   - utter_greet
* affirm
   - health_form
   - form{"name":"health_form"}
   - form{"name":null}
   - utter_slot_values
* thankyou
   - utter_no_worries
   - utter_goodbye

## story: stop
* greet
   - utter_greet
* affirm
   - health_form
   - form{"name":"health_form"}
* out_of_scope
   - utter_ask_continue
* deny
   - action_deactivate_form
   - form{"name":null}
   - utter_goodbye

## story: continue
* greet
   - utter_greet
* affirm
   - health_form
   - form{"name":"health_form"}
* out_of_scope
   - utter_ask_continue
* affirm
   - health_form
   - form{"name":null}
   - utter_slot_values

## story: ask health questions
* greet
   - utter_greet
* affirm
   - health_form
   - form{"name":"health_form"}
* ask_exercise
   - utter_exercise_info
   - health_form
   - form{"name":null}
   - utter_goodbye

## story: no survey
* greet
   - utter_greet
* deny
   - utter_goodbye

## story: say goodbye
* goodbye
   - utter_goodbye

## story: bot challenge
* bot_challenge
   - utter_iamabot