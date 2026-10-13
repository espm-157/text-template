# Text as Data Module: Detailed Rubric

Total: 20 points

You may automate any step that a model can do well. You are graded on the guidance you give the
models, the judgments you make about their output, and the record of how you worked.

## 1. Making the question precise (**4 points**)

**4 points**: The notebook states, in your own words, the decisions that turn the question into
something a computer can answer, and defends each one:

- which documents count as listing decisions, and how you checked that the set is complete;
- what counts as the agency finding that climate change is a threat, as distinct from mentioning
  it, with examples of paragraphs on each side of the line;
- how a judgment about a paragraph becomes a judgment about a rule.

## 2. Disagreeing with a model (**5 points**)

**5 points**: The notebook documents specific cases where you disagreed with a classification from
Laya, an answer from RAG, or a record from extraction:

- you read the source paragraph;
- you decided who was right;
- you explain what the disagreement tells you about the tool.

At least some of these come from your own reading. Where you did ask a model to judge, the notebook
says so.

## 3. Choosing tools (**4 points**)

**4 points**: For each step, the notebook says which tool you used and why. Claims about speed, cost
and accuracy are measured, not asserted. The notebook gives your own sense of when you would reach
for a regular expression, a classifier, search, RAG, or extraction, based on what happened here.

## 4. Result and reconciliation (**3 points**)

**3 points**: The notebook gives an answer to the question with a figure, and compares it with
Delach et al. Before attributing any difference, it establishes what each source counts: which
documents, which species, and which years.

## 5. Process (**4 points**)

**4 points**: The repository includes your conversations with your coding agent (in Kilo Code, use
the task's export button and save the files in `prompts/`). The prompts show the guidance you gave:
definitions, corrections, and decisions to overrule or redirect the agent. Commits show how the
work developed.

The README is updated with authorship information, a correct badge link, and a description of what
you found. The repository passes the notebook check on GitHub Actions.

## Failure conditions

The notebook presents fabricated data, or numbers or quotations that do not come from the sources,
as if they were real. (Automatic fail)

The notebook presents a model's judgment as your own: for example, labels or reflections written by
a model and described as your reading. Using a model for these is allowed; misrepresenting who made
the judgment is not.
