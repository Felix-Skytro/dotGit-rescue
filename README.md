# dotGit-rescue
A startup command for linux servers if for some reasons the .git directory broke

Light Script:
if [[ -d .git ]]; then if [[ -z "$(ls -A .git)" ]]; then echo ".git is empty, reinitializing..."; git init; else echo ".git is not empty, manual cleanup needed."; fi; else echo ".git not found, initializing..."; git init; fi; read -p "Add remote repository? (y/n): " add_remote; if [[ $add_remote == "y" || $add_remote == "Y" ]]; then read -p "Enter remote URL: " remote_url; git remote add origin "$remote_url"; echo "Remote added: $remote_url"; fi


Hard:
Coming Soon..
