# GES 778 midterm project

2024-03-06

## Intro

This is a scaffold for your GES 778 midterm project. To get you started,
it contains the following files:

    .
    ├── code
    │   ├── 01_eda.qmd
    │   ├── 02_sketches.qmd
    │   └── 03_final_draft.qmd
    ├── data
    ├── docs
    │   ├── abstract.md
    │   └── technical_notes.md
    ├── midterm.Rproj
    ├── plots
    ├── _quarto.yml
    ├── README.md
    └── utils
        └── plotting_utils.R

    5 directories, 9 files

## Requirements

You will hand in the following, all within this repo:

- A final draft notebook with 2 to 3 final charts:
  - 3 charts if they are all fairly standard chart types (bar charts,
    line charts, scatterplots, histograms, etc)
  - 2 charts if one is more complex or experimental (Sankey diagrams,
    treemaps, network diagrams, isotypes, etc.)
- EDA and sketch notebooks
- Technical notes. This is a short, informal document (bulletpoints are
  great) laying out details of what you did, what technical decisions
  you made and why, and guidance on working with your code further.
  Think of it as notes you’ll reference when you use parts of your code
  at your next job or your capstone a year from now, or how you’ll
  acquaint another developer with your code.
- Abstract. This is a short, non-technical document giving a high-level
  overview of the project explaining your decisions to a non-coder,
  focused more on what you set out to do, how you revised it, and how
  you incorporated feedback. If you were to send your project as a work
  sample for a job, this would be its cover letter.

## Code

Some good coding practices you should use here:

- Separate concerns in separate places:
  - Utilities and snippets go in scripts in the `./utils` folder
  - EDA, sketches / rough drafts, and final versions go in different
    notebooks
  - If you have any additional data, it goes in the `./data` folder
  - When you export final copies of plots, they go in the `./plots`
    folder
- Use notebooks and knit / render them often
- Write comments & notes in your notebooks as you work, so your final
  write-up will be easier
- Make git commits often and push them to GitHub often, with informative
  commit messages (e.g. “Adjust colors in EDA charts” rather than “Work
  on charts”)

## Exploratory data analysis / visualization

Your first step is to **figure out what you’re interested in
visualizing**. Look through the datasets in the justviz package and
decide which one(s) you’d like to work with (you are free to join
datasets or do additional calculations if you’d like), and which
variables you’ll use. Conduct EDA, focusing on your chosen variables.
Refer back to [chapter 10](https://r4ds.hadley.nz/eda) of *R for Data
Science* for an overview of what might go into EDA, and the [ggplot
documentation](https://ggplot2.tidyverse.org) for specific help. How you
explore a dataset depends on the data itself, but in general this
notebook should include:

- Distributions (boxplots, histograms, etc)
- Descriptive statistics (start by calling `summary` on your data frame)
- Patterns between variables, if applicable (scatterplots)

Take notes as you go—what you’re doing, why you’re doing it, and
especially what you find in the process. By the time you’re done, you
should have a sense of what story you want to tell.

## Sketches

In your sketches notebook, you’ll take what you’ve decided you want to
show, and you’ll work through different ways to approach it. You might
want to choose some of your EDA charts as a starting point, or do
something new based on your findings. This will involve **sketching on
paper first**. Mark up your drawings with some details to help you
organize your thoughts (what goes on the axes, what subsets of the data
you might be using (e.g. each point in your scatterplot is one tract,
each bar in your bar chart is a county, etc)).

Then **sketch with code** to figure out what you’ll want for your final
charts. Some examples of moving from EDA to a sketch are:

| EDA                                                                 | Sketch                                                                                                             |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Scatterplot of 2 variables from the ACS dataset (x and y encodings) | Scatterplot of those same 2 variables, filtered for just metro areas and adding a 3rd variable via a size encoding |
| Stacked bar chart                                                   | Separating those same bars with facets instead of stacking them                                                    |
| Side-by-side (dodged) bar chart to show differences between groups  | Dot chart to show the same differences, but with better focus on the range of values in the dataset                |
| Charts without clean, formatted labels and captions                 | Charts with formatted labels                                                                                       |

If you’re doing any calculations or changing any variables and want to
write them out before moving on to your final visualizations, this is a
good place to do that.

By the end of this notebook, you will have decided on 2 to 3 charts that
you’ll finalize, and you’ll know what story you want to tell and how.

## Final draft

In your final draft, you’ll have just a few chunks of code, 1 per chart.
Your project will be graded on each chart in this notebook, so keep your
experimentation in the sketches notebook.

At this point you will have decided on everything applicable in the
[decisionmaking
checklist](https://umbc-viz.github.io/ges778/decision_checklist.html),
and now you’ll just be implementing those decisions as cleanly as
possible.

## Check-ins

We’ll check in each week about your progress, so you’ll always have a
sense that you’re on the right track. If you’re working steadily on
this, there won’t be any surprises when it comes to grading; if you wait
until the last minute, you will have missed out on feedback.
