# Merge Conflict Notes

## What happened

The tagline line of README.md (directly under the title) was edited
independently on two branches:

- On main, the line was changed to:
  "Predicting red wine quality scores from physicochemical properties using regression models."
- On proposal, the line was changed to:
  "A regression project estimating red wine quality from lab-measured chemical properties."

Because both branches modified the same line relative to their common
ancestor commit, Git could not automatically decide which version to keep
when merging proposal into main via the pull request. GitHub flagged the
file with conflict markers (<<<<<<<, =======, >>>>>>>) separating the
two competing versions.

## How it was resolved

Using GitHub's web-based conflict editor, I compared both versions and
manually combined them into a single line that kept the clarity of the
main version while incorporating the "lab-measured" phrasing from the
proposal version:

"Predicting red wine quality scores from physicochemical, lab-measured properties using regression."

I removed the conflict markers, leaving one clean line, then marked the file
as resolved and committed the merge.

## Why this approach

Rather than picking one branch's wording outright, merging the phrasing
preserved the intent of both edits while keeping the sentence readable.
