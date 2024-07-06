## Mosh Hamedani
[YouTube channel](https://codewithmosh.lt.emlnk9.com/Prod/link-tracker?redirectUrl=aHR0cHMlM0ElMkYlMkZ3d3cueW91dHViZS5jb20lMkZjJTJGcHJvZ3JhbW1pbmd3aXRobW9zaA==&sig=5NEFJgW4YLJfPviWzUcv4CsrQoXqPgddYM7smT3BpBf5&iat=1720289800&a=%7C%7C89545604%7C%7C&account=codewithmosh%2Eactivehosted%2Ecom&email=0DP%2F3BzpkUQ6DJi2DFaTUgoU3O6Au0ieJ8EERdERXKty%3AopRBaUCHxboUBq4%2Bp9rrSAkC%2FeR3uOSb&s=033952ba7711342a336c13c47f088047&i=655A883A24A5879)
<br>


# Git Commands

## configuration

**git config --global -e**: open git global configuration file  
<br>

## pre-commit hooks
A Git pre-commit hook is a script that runs automatically when you run the git commit command. If the script exits with a non-zero status, the commit is aborted. This can be useful for running tests, checking for code style issues, or other checks before a commit is made.  Here's a basic example of how to define a pre-commit hook:  
- Navigate to the **.git/hooks** directory in your Git repository.
- Create a new file named **pre-commit** (without any extension).
- Make the file executable by running **chmod +x** pre-commit.
- Open the pre-commit file in a text editor and add your script:
```
#!/bin/bash

echo -e "\033[1;33mpre-commit hook: Running 'cybr pr'.................\033[0m"
cybr pr
if [ $? -ne 0 ]; then
    echo -e "\033[1;31mpre-commit hook: 'cybr pr' errors found. Aborting commit.\033[0m"
    exit 1
fi
```
- To run commit avoiding pre-commit hook use **--no-verify** option
  
**Formatting:**
- \033[1;33m sets the text to **yellow and bold**.
- \033[1;31m sets the text to **red and bold**.
- \033[0m resets the text formatting.


<br>
      
## stash

**git stash push -m "my_stash_name"**: Stash with name - "my_stash_name"

**git stash list**: List available stored stashes

**git stash pop stash@{n}**: Pop of chosen stash

Reference: https://stackoverflow.com/questions/11269256/how-do-i-name-and-retrieve-a-git-stash-by-name
<br>


