# Text as Data Module: Detailed Rubric

Total: 20 points (of 29 available -- this allows multiple paths through the module)

Baseline tasks in every part are expected. **🧗 Go deeper** tasks are optional, and are the main
route to the points beyond 20.

## 1. Text Handling and Regular Expressions (**4 points**)

**4 points**: The corpus is assembled from the Federal Register API and its scope is stated:
which rules, which years, and what was excluded and why. The title filter has been audited
and corrected, with the misclassified titles counted. Paragraph splitting is checked against
the published rule. Regular expressions are chosen deliberately, and the notebook says what
each pattern catches, what it misses, and how the student found out.

## 2. Models as Measurement Instruments (**5 points**)

**5 points**: The classifier, retrieval, RAG and extraction steps are each *evaluated*, not
just run.

  - Hand labels exist, were made before looking at the model's answers, and are used to judge
    the classifier. The threshold on `p_threat` is chosen and defended with evidence.
  - Every citation in at least two RAG answers is checked against the cited paragraph.
  - Extracted rows are audited against the rule text, and the `evidence` field is checked
    with code.
  - Disagreements are resolved by reading the source, and the student says who was right.

## 3. Code Quality and Tool Choice (**4 points**)

**4 points**: The code is concise and semantically meaningful, and does not introduce
libraries or methods beyond what the task needs.

_Tool choice is part of code quality._ The notebook uses the cheapest tool that answers each
question (a regular expression where a pattern suffices, a classifier as a filter before a
language model), and can say why. Expensive model calls are cached to `data/` rather than
repeated.

Avoid common LLM-based code-junk that does not follow best practices in data science notebooks:
  - Do not use `print` statements in code cells, except to read text.  The final value on a cell is auto-printed by Jupyter.
  - Code should not include unnecessary error handling, such as `try` statements.
  - Code should not create function definitions unless they serve a clear use in making the code more concise and readable.
  - Do not include code comments in most cases.  Use markdown cells to explain the overall logic and flow of the notebook.
  - Each code cell should do one thing, and be clearly labeled with a markdown cell above it to explain what it does.

## 4. Verification and Scientific Judgment (**5 points**)

**5 points**: The student can answer the question _how do I know these numbers are right?_
for their own analysis.

  - The verification blocks are completed substantively, in the student's own words.
  - The distinction between *mentioning* climate change and *finding it a threat* is kept
    throughout, and the headline figure says which it shows.
  - The comparison with Delach et al. establishes what each source counts (documents,
    species, years) before attributing any difference, and species are matched with care.
  - At least one concrete model error is documented, with how it was found.

## 5. Narrative (**3 points**)

**3 points**: The notebook tells a clear story about climate change and the Endangered Species
Act. Instructor headings like "Task 2.1" are replaced by topical headings. Figures are
described in prose. Reflection responses give an honest account of what the models got wrong
and of what the student contributed.

## 6. Use of GitHub (**4 points**)

**4 points**:

README file is updated with:
  - Authorship information
  - GitHub Actions badge, with correct link to repository
  - Updated description of repository overview.

Repository passes the auto-check on GitHub Actions. Large intermediate files (`data/`) are not
committed.

Clear, clean record of GitHub commits, appropriate git log messages.

## Failure conditions

The notebook fabricates data, or presents fictitious, made-up, or "example" numbers in
tables or charts as if they are real. (Automatic fail)

This applies without change to text and numbers produced by a model. A quotation that does
not appear in the source, a citation to a paragraph that does not say what is claimed, or a
hand-label column that was really filled in by a model, presented as genuine, is the same
failure. Checking is your job, and it is the job this module exists to teach.
