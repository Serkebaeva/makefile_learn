# The "Golden Standard" for Shared Projects

If you want the runner to be instantly available and zero-setup for anyone who clones your repo, the Local Wrapper Script is actually the best choice. 

1. Create a file named do (or run) in your root directory.

2. Paste this logic
```
#!/bin/bash
# Check if a number was provided
if [ -z "$1" ]; then
    echo "Usage: ./run [number] [target]"
    exit 1
fi

MAKE_FILE="makefile$1"
shift 

# Run make, passing the remaining arguments
make -f "$MAKE_FILE" "$@"
```
3. Make it executable
`chmod +x run`

4. Commit it to git
```
git add run
git commit -m "Add project runner"
```

---------------------------
VS Code Markdown Preview: Press <span style="font-size:1.1em; color:#87CEEB;"><em><ins>Ctrl+Shift+V</ins></em></span> to open a live preview.
--------------------------
### Errors during project:
```
**The problem was:** makefile5 didn't specify a default target, so when you ran `./run 5`, make would only create the obj directory (due to the directory prerequisite) but wouldn't compile the object files because the hellomake target was never explicitly requested.

**The solution:** I added `.DEFAULT_GOAL := hellomake` to makefile5. Now `./run 5` automatically builds the hellomake target, and the object files are correctly created in obj.
```
*!!!I created **makefile6** —> which is correct and left makefile5 with error to learn from….!!!*