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

 Summary table
 

 | Command                 | What it does                   |                            |
| ----------------------- | ------------------------------ | -------------------------- |
| `grep 'Sales'`          | Lines with "Sales"             |                            |
| `grep -v 'Sales'`       | Lines without "Sales"          |                            |
| `grep '^A'`             | Lines starting with "A"        |                            |
| `grep '0$'`             | Lines ending with "0"          |                            |
| `grep -c 'Engineering'` | Count lines with "Engineering" |                            |
| `grep -i 'marketing'`   | Case-insensitive search        |                            |
| `grep -n 'Sales'`       | Show line numbers with "Sales" |                            |
| \`grep -E 'Sales        | HR'\`                          | Lines with "Sales" or "HR" |


✅ 1️⃣ Replace "Engineering" with "Tech"

sed 's/Engineering/Tech/' employees.txt

✅ 2️⃣ Replace "Sales" with "Business" globally (all occurrences per line)

sed 's/Sales/Business/g' employees.txt

✅ 3️⃣ Delete lines containing "HR"

sed '/HR/d' employees.txt


✅ 4️⃣ Print only lines containing "Engineering" (like grep)


sed -n '/Engineering/p' file1.txt

✅ 5️⃣ Insert a line before each "HR" line

sed '/HR/i -----HR Department Starts-----' employees.txt


✅ 6️⃣ Append a line after each "Marketing" line


sed '/Marketing/a -----Marketing Ends-----' employees.txt

✅ 6️⃣ Append a line after each "Marketing" line


sed '/Marketing/a -----Marketing Ends-----' employees.txt


✅ 7️⃣ Change whole line containing "Charlie"


sed '/Charlie/c Charlie,Support,6600' employees.txt


✅ 8️⃣ Replace "Engineering" with "Tech" directly in the file (in-place)

sed -i 's/Engineering/Tech/g' employees.txt


⭐ Summary table

| Command           | What it does              |
| ----------------- | ------------------------- |
| `s/old/new/`      | Replace first occurrence  |
| `s/old/new/g`     | Replace all occurrences   |
| `/pattern/d`      | Delete matching lines     |
| `-n /pattern/p`   | Print only matching lines |
| `/pattern/i text` | Insert line before match  |
| `/pattern/a text` | Append line after match   |
| `/pattern/c text` | Change whole line         |
| `-i`              | Edit file in place        |



✅ 1️⃣ Print all employee names

awk -F',' '{print $1}' employees.txt

✅ 2️⃣ Print names and departments

awk -F',' '{print $1, $2}' employees.txt

✅ 3️⃣ Print employees with salary > 6000

awk -F',' '$3 > 6000 {print $0}' employees.txt



 ✅ 7️⃣ Change whole line containing "Charlie"

awk -F',' '$2 == "Engineering" {print $1}' employees.txt


✅ 5️⃣ Calculate and print total salary

awk -F',' '{sum += $3} END {print "Total Salary =", sum}' employees.txt

Print line number and entire line

awk -F',' '{print NR $0}' file1.txt

Print only department names (unique)

awk -F',' '{print $2}' employees.txt | sort | uniq


✅ 8️⃣ Add "Employee:" prefix to each name

awk -F',' '{print "Employee:", $1}' employees.txt

✅ 9️⃣ Print highest salary

awk -F',' 'BEGIN {max = 0} {if ($3 > max) max = $3} END {print "Max Salary =", max}' employees.txt

✅ 9️⃣ Print highest salary

awk -F',' 'BEGIN {max = 0} {if ($3 > max) max = $3} END {print "Max Salary =", max}' employees.txt


✅ 10️⃣ Print names and add "High Salary" tag if salary > 6500


awk -F',' '{if ($3 > 6500) print $1, "- High Salary"; else print $1}' employees.txt

 
