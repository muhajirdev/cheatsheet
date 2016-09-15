`git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch bower_components -r' --prune-empty --tag-name-filter cat -- --all`
