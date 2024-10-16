## File handling

- Separator `IFS=$'\n'`

```bash
IFS=$'\n'
for line in $(cat certi.txt)
do
$(mv $line path/dst/)
done
```

- Read the lines in the `certi.txt` with new line \n as separator file and move it to destination folder.
