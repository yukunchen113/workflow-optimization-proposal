# workflow-optimization-proposal: My ideas, open for discussion.
Document on cross team dependency sharing

## Goal: maximize effective dev time
How?
1. Maximize reusage of code
2. Minimize library maintenance by design

## Discoverability: Maximize reusage of code

### Step 1: Spotlight step
- based on existing workflows find out the system components which are heavily used
- provides rough preemptive quantitative measure on how likely a given team will:
  1. already have a component library implemented (lowers current team cost)
  2. need this library in the future (shows increase in benefit of making library)

### Step 2: In-Team Action
- for an external dependency needed in a project
  - check if library exists already been implemented for that system component (likelihood is based on spotlight)
    - if yes, extend that library
  - if no, then create your own library according to guidelines on making easy-to-extend (low overhead) libraries (see Seamless Extensions section below)

### Step 3: Library Promotion
- demo library to that system component stakeholders (identified via Spotlight Step above)
  - if others find it useful, share it with them
    - if they are familiar with the library guidelines already, almost no explanation is needed!

### Step 4: Library Extension Promotion (Minimize library maintenance)
- Ties in with Seamless extensions section
- team specific library components will be added into library only if sufficiently requested (can otherwise still be shared individually cross team)
  - this can be predicted via the Spotlight step in Discoverability above.
  - this is to minimze the need to maintain the library, and only keeping the heavy hitters (80:20 rule)



## Seamless Extentions: Minimize library maintenance by design

Two pillars

- standard way to extend code (via data driven design and functions/functors)
  - this is so that personal components of the library can be immediately added in 
  - no reformatting, no refactoring, no conforming after code has been written
- team specific library components will be added into library only if heavily requested (and can otherwise still be shared seperately)
  - this can be predicted via the Spotlight step in Discoverability above.
  - this is to minimze the need to maintain the library, and only keeping the heavy hitters (80:20 rule)


