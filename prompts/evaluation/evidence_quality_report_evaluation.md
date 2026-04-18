## Caption: 
This prompt is used to produce the evidence quality score


## Prompt: 
You are asked to provide a ranking for each category on an Likert scale (strongly disagree, disagree, neither agree nor disagree, agree, strongly agree) regarding the points in the report.

ASPECTS:

- Does this point affect the level of fraud suspicion, either by increasing or decreasing it? Both outcomes should be scored positively, as long as the point alters the suspicion level.
- This point was relevant to the investigation case.
- This point provided me with new knowledge or confirmed unbased knowledge about the case.
- This point logically aligns with the rest of the report.


NOTICE:

- You must give a rating to ALL of the evidence in ALL of the steps in the report.
- Please remember that inaccurately scoring a bad report as a good report may affect the future of your employment, so be critical about your scoring method.
- The report consists of both supporting fraud evidence and supporting legitimate evidence; both types of points should be rated by the same standards.
- The order of the evidence in the report shouldn't matter for your scoring.
- When ranking each aspect, try to isolate it and not take any other aspects into consideration.


Example JSON Rankings
    The unfiltered report:
        - Step 1:
            Evidence:
                - The transaction amount is within the upper typical range for similar merchants.
        - Step 2:
            Evidence:
                - The distance between the cardholder's house and the transaction location is under 100 km.
        - Step 3:
            Evidence:
                - It falls within usual transaction hours, not an outlier.


  ```json
  {"report_evaluation" : [
    {
        "evidence": "The transaction amount is within the upper typical range for similar merchants."
        "impact_on_fraud_suspicion_level": "agree,"
        "relevant_to_investigation_case": "strongly agree,"
        "providing_new_knowledge": "disagree,"
        "logical_alignment": "agree"
    },
    {
        "evidence": "The distance between the cardholder's house and the transaction location is under 100 km."
        "impact_on_fraud_suspicion_level": "neither agree nor disagree,"
        "relevant_to_investigation_case": "agree,"
        "providing_new_knowledge": "agree,"
        "logical_alignment": "Agree"
    },
    {
        "evidence": "It falls within usual transaction hours, not an outlier."
        "impact_on_fraud_suspicion_level": "agree,"
        "relevant_to_investigation_case": "strongly agree,"
        "providing_new_knowledge": "Disagree,"
        "logical_alignment": "Strongly Disagree"
    },
]}

  ```
Now, here is the report that I want you to evaluate and provide a rating for:

{report_to_evaluate}
