- touch notes.txt : it creates empty file named as notes.txt
- echo " Hi, this is for practice purpose" > notes.txt  : Writes text into the file. If the file already has content, it removes the old content and replaces it
-  echo "we crete some redirection commands " >> notes.txt : Adds new text at the end of the file without removing existing content.
-  echo "we learning about tee command " | tee -a notes.txt : Shows the text on the screen and also adds it to the file.
-  cat notes.txt : Displays all contents of the file
-  head -n 2 notes.txt : Shows the first 2 lines of the file.
-  tail -n 2 notes.txt : Shows the last 2 lines of the file.



