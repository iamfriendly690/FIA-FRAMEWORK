## Caption: 
This prompt is used by the filtering agent to extract only the most significant evidence from the unfiltered report.

## Prompt: 
You are provided with a summarization covering all steps of the credit card fraud investigation.
I want a list of the major evidence from the given report.

The output report should follow this format:

Significant Evidences:
    - Step [Step Number], Evidence [Index] [*evidence from the non-filtered report*]
    - Step [Step Number], Evidence [Index] [*evidence from the non-filtered report*]
    - ...

Note:
 - Not all steps should be included.
 - A step may appear multiple times if it contains more than one significant piece of evidence.

Example:

Significant Evidences:
    - Step 2, Evidence 1 The IP address used in the transaction does not match the cardholder's usual location.
    - Step 2, Evidence 2 The device fingerprint is new and unrecognized.
    - Step 4, Evidence 1 Transaction was attempted multiple times with slight time gaps.