# CSP-Based Sudoku Solver (AC-3 + Forward Checking + Backtracking)

## Overview

This project implements a Constraint Satisfaction Problem (CSP) solver for Sudoku using:

* Backtracking Search
* Forward Checking
* AC-3 (Arc Consistency Algorithm 3)
* MRV (Minimum Remaining Values) heuristic

It solves Sudoku puzzles of varying difficulty: easy, medium, hard, and very hard.

---

## Features

### CSP Techniques Used

* AC-3 Algorithm
  Ensures arc consistency before and during search.

* Forward Checking
  Removes invalid values early to reduce search space.

* Backtracking Search
  Explores valid assignments recursively.

* MRV Heuristic
  Selects the variable with the fewest remaining values first.

---

### Robust Input Handling

* Supports `.txt` Sudoku files
* Safely parses boards and ignores formatting issues

---

### Performance Tracking

The solver tracks:

* Number of backtracking calls
* Number of failures



## How to Run

### Step 1: Prepare Input Files

Each file must contain a 9×9 Sudoku grid.

Example:

```
530070000
600195000
098000060
800060003
400803001
700020006
060000280
000419005
000080079
```

Use `0` for empty cells.


## Algorithm Flow

1. Read Sudoku board from file
2. Initialize CSP domains
3. Apply AC-3 preprocessing
4. Start backtracking search
5. Use:

   * MRV heuristic
   * Forward checking
   * MAC (Maintaining Arc Consistency)
6. Return solved board or failure


## Key Concepts

### CSP (Constraint Satisfaction Problem)

Sudoku is modeled as a CSP where:

* Variables represent cells
* Domains represent possible values (1–9)
* Constraints enforce row, column, and 3×3 box rules

---

### AC-3

Removes inconsistent values before and during search to enforce arc consistency.

---

### Forward Checking

Eliminates invalid values immediately after each assignment.

---

### MRV Heuristic

Chooses the variable with the smallest remaining domain to reduce branching.

---

## Possible Improvements

* Add Degree Heuristic
* Add LCV (Least Constraining Value)
* Build a GUI using Tkinter or PyGame
* Benchmark performance across puzzles
* Add unit tests for CSP components


