## GitHub CLI

provides a way to interact with GitHub repositories and perform various actions directly from the command line. Here are some commonly used GitHub CLI commands:

## Authenticate with GitHub:
 
   gh auth login
 
## Create a new repository:
 
   gh repo create
 
## Clone a repository:
 
   gh repo clone <repository>
 
## List repositories:
 
   gh repo list
 
## View repository details:
 
   gh repo view <repository>
 
## Create a new branch:
 
   gh repo create <branch>

## Switch to a different branch:
 
   gh repo fork <branch>
 
## Create a new pull request:
 
   gh pr create
 
## View pull requests:
 
   gh pr list
 
## Merge a pull request:
  
    gh pr merge <pull-request-number>
  
 ## View issues:
  
    gh issue list
  
## Create a new issue:
  
    gh issue create
  
 ## View the status of a workflow:
  
    gh workflow view
  
## Run a workflow manually:
  
    gh workflow run
  
## View and manage actions:
  
    gh action list
    gh action view
    gh action disable
    gh action enable
    gh run list
  
## Note
These are just a few examples of the commands available in GitHub CLI. You can explore more commands and their options by running `gh --help` or `gh <command> --help` to get detailed information and usage instructions for a specific command.