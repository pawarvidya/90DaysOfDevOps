## Files Created

- devops.txt - Empty file created using touch
- notes.txt - Created using echo with sample content
- script.sh - Shell script created using vim
- project/ - Directory created for permission practice

## Permission Changes

| File/Directory | Before | After |
|----------------|--------|-------|
| script.sh | -rw-r--r-- | -rwxr-xr-x |
| devops.txt | -rw-r--r-- | -r--r--r-- |
| notes.txt | -rw-r--r-- | -rw-r----- |
| project/ | drwxr-xr-x | drwxr-xr-x |


## Commands Used

```bash
# Create files
touch devops.txt
echo "Linux File Management Practice" > notes.txt
vim script.sh

# Verify files
ls -l

# Read files
cat notes.txt
vim -R script.sh
head -n 5 /etc/passwd
tail -n 5 /etc/passwd

# Check permissions
ls -l devops.txt notes.txt script.sh

# Modify permissions
chmod +x script.sh
./script.sh

chmod a-w devops.txt

chmod 640 notes.txt

mkdir project
chmod 755 project

# Verify changes
ls -l
ls -ld project
```

---

## What I Learned

1. Learned how to create files using `touch`, `echo`, and `vim`.
2. Understood Linux file permissions (`r`, `w`, `x`) for Owner, Group, and Others.
3. Learned how to use the `chmod` command with both symbolic (`+x`, `a-w`) and numeric (`640`, `755`) permissions.
