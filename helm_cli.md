## Helm Cheat sheet 

Here are some helm command to get you started.

#   List available chart repositories:
 
 helm repo list
 
#   Add a new chart repository:
 
 helm repo add <repository-name> <repository-url>
 
#   Remove a chart repository:
 
 helm repo remove <repository-name>
 
#   Update a specific chart repository:
 
 helm repo update <repository-name>

#   Check the dependencies of a chart:
 
 helm dependency list <chart-directory>
 
#   Build the dependencies of a chart:
 
 helm dependency build <chart-directory>
 
#   Dry run an installation to see the changes without actually deploying:
 
 helm install --dry-run --debug <release-name> <chart-name>
 
#   Get the notes associated with a release after installation:
 
 helm get notes <release-name>
 
#   Get the values used in a release:
 
 helm get values <release-name>
 
#   Package a chart with specific values:

helm package --values <values-file> <chart-directory>

#   Verify the syntax of a chart without installing it:

helm lint <chart-directory>

#   Test a release by running the associated tests:

helm test <release-name>

#   Create a new chart from an existing template:

helm create --starter <starter-name> <chart-directory>

#   Check the version of Helm:

helm version

#   Display detailed information about a release:

helm get all <release-name>


## Notes 

consult the official Helm documentation or run `helm --help` or `helm <command> --help` for more information on each command and its available options.