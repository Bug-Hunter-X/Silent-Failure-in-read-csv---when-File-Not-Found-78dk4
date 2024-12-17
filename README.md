# R Bug: Silent Failure of read.csv()

This repository demonstrates a common, yet easily missed, error in R: the silent failure of `read.csv()` when the specified file does not exist.  The code attempts to read a CSV file; however, if the file is not found, `read.csv()` returns a NULL value without throwing an error or warning. This can lead to cryptic errors later in the code when the program tries to use the non-existent `data`.

The `bug.r` file showcases the problematic code, and `bugSolution.r` provides the solution.

## How to reproduce

1.  Clone this repository.
2.  Run `bug.r`. Observe that no error is thrown, even if `my_data.csv` does not exist.  Any subsequent attempts to use `data` will fail silently or with confusing errors.
3.  Run `bugSolution.r`.  This version includes robust error handling.