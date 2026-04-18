## Caption:
Given the predicted label from the 'Detective Agent' and the output from the 'unfiltered_report_generation' prompt, this prompt outputs the supporting prediction steps.

## Prompt:
You are provided with a detailed summary covering all steps of a credit card fraud investigation.
Your task is to extract and list the major pieces of evidence highlighted in the report, which supports the investigators prediction: {predicted_label}.

Output Report Format:

Significant Evidence:
Step [Number]:
    - Evidence 1
    - Evidence 2
    ...
Step [Number]:
    - Evidence 1
    - Evidence 2
    ...
...
(Continue listing as necessary)

Guidelines:
Include only the steps that present significant evidence.

Summary Report:
{unfiltered_report_generation_output}