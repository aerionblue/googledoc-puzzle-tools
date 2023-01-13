# googledoc-puzzle-tools
Scripts and functions for puzzle hunt (two words) puzzles.

If you're on my team, this extension is installed by default on our Google Workspace domain, but you have to manually enable it on each sheet where you want to use it. Just click `Extensions > Puzzle Tools > Enable for this sheet`.

# Features

## Custom Menu Items
*  *Square Cells* - Make all selected cells squares of some size. 20 is good for letters.
*  *Symmetrify Grid* - Make the selected cells have symmetry with regard to background color.
    Rotational (standard crossword) and bilateral are both supported.
*  *Formatting Shortcuts* - Apply some commonly-used formatting (and conditional formatting) to cells.
    * *Crossword grid* - Prepare a range of columns to hold a crossword grid.
       Most notably, sets the conditional formatting so that a cell whose
       value is "/" will become a black square.

## Added functions

Function File              | Function Name     | Usage                             | Purpose
-------------------------- | ----------------- | ---------------------------       | --------------------------------------------------
sheet_functions/caesar.js  | CAESAR_SHIFT      | CAESAR_SHIFT(string, shift)       | Shift every letter in a string by a certain amount
sheet_functions/general.js | INDEX_IN_ALPHABET | INDEX_IN_ALPHABET(index)          | Return the nth letter in the alphabet from an index.
sheet_functions/general.js | BINARY_TO_NUMBER  | BINARY_TO_NUMBER(string)          | Converts a binary string into a decimal number.
sheet_functions/general.js | TERNARY_TO_NUMBER | TERNARY_TO_NUMBER(string)         | Converts a ternary string into a decimal number.
sheet_functions/general.js | FROM_MORSE        | FROM_MORSE(string, [dot], [dash]) | Converts a string of Morse to plaintext. Supports optional dot and dash characters.
sheet_functions/general.js | TO_MORSE          | TO_MORSE(string, [delimiter])     | Converts a plaintext string to Morse.  Separates characters in output with optional delimiter.
sheet_functions/general.js | SPLIT_INTO_CELLS  | SPLIT_INTO_CELLS(string)          | Put each character of the input into its own cell to the right.
sheet_functions/general.js | ANSWERIZE         | ANSWERIZE(string, [spacesOnly])   | Strip non-alpha characters and uppercase the input.  Optionally strip spaces only.
sheet_functions/general.js | IDX               | IDX(string, indexOrList)          | Index the Nth letter of the given string. You usually want to `ANSWERIZE` the string first. `indexOrList` can be a space-delimited list of numbers, if you want to index multiple letters at once.
sheet_functions/general.js | ALPHAGRAM         | ALPHAGRAM(string, [results])      | Alphabetizes the letters of a string. You can use this, e.g., to check whether two strings are anagrams of each other (they will have equal alphagrams).
sheet_functions/general.js | ANAGRAM           | ANAGRAM(string, [results])        | Look up anagrams and return n results (default is 10)
sheet_functions/general.js | NUTRIMATIC        | NUTRIMATIC(string, [results])     | Look up nutrimatic results for a query and return n results (default is 10)
