⭐ Quick summary table

| Tool     | Main purpose           | Typical use cases                        |
| -------- | ---------------------- | ---------------------------------------- |
| **grep** | Search & filter lines  | Find lines with “error”, count matches   |
| **sed**  | Edit & transform lines | Replace words, delete lines, insert text |
| **awk**  | Process columns/fields | Print columns, filter rows, calculate    |

grep command operation
----------------------------------------------------------------------------

 Find all employees in Engineering?

 grep 'Engineering' employees.txt

Find lines starting with "A"?

grep '^A' employees.txt

 Find lines ending with salary 6500

 grep '6500$' employees.txt


Find lines not containing "Sales"

grep -v 'Sales' employees.txt


Show line numbers containing "Sales"

grep -n 'Sales' employees.txt


 Count lines containing "Engineering"


 grep -c 'Engineering' employees.txt


Ignore case when searching for "marketing"


grep -i 'marketing' employees.txt


 Highlight the matching word in color (if your terminal supports)

 grep --color=always 'Engineering' employees.txt



Find lines containing either "Sales" or "HR" using -E

grep -E 'Sales|HR' employees.txt



