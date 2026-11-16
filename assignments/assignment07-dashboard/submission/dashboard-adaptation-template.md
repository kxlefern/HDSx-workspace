# Dashboard Adaptation Note

## Audience

A public health analyst preparing a short briefing on descriptive BMI patterns.

## Dashboard Question

Among adults aged 20-80, how does mean BMI vary across NHANES cycles for one selected income group?

## Control And Visualization

- Control or interaction: selected_income in the dashboard-control chunk
- Visualization affected: summary table, plot title, line plot of mean BMI by NHANES cycle 
- What changes when the control changes: when selected_income changes, the income group used to filter the data also changes. Table rows, plot title, and line plot points update to the selected income group.

## Before And After

| Original text | Revised text | Why the revision helps |
|"For example, change the line to `selected_income <- "Middle Income"` — the other valid value in the classroom dataset is `"High Income (>3.5)"`. Copy the value exactly, including the quotes and any parentheses."|"To change the income group, edit the value of `selected_income` in the chunk above and render again. Use one of the exact labels listed in the chunk's output (`available_income_groups`), including the quotes and any parentheses, for example `"High Income (>3.5)"`. If the label doesn't match exactly, the dashboard falls back to the first group, so confirm that the plot title names the group you intended." | The original implied a shortened label and did not warn that a mismatched label silently falls back to the first group. The revision points to the exact labels and names the fallback, so an analyst is less likely to present the wrong group. |

## Test Result

I picked a different selected income and rendered it. It gave me the appropriate changes with respect to the change in selected income as opposed to the other selected income. 

## Limitation

This dashboard displays unweighted, descriptive mean BMI for adults aged 20-80 in the classroom NHANES equity dataset, and therefore does not support causal claims about income and BMI. 

## Privacy Check

The preview shows aggregate cycle-level n and mean BMI with no row level records or data previews. No small-cell interpretations are made. 
