```
github-issue - Tool for interacting with GitHub Issues from the command line

Usage: github-issue [options] command [issues]

Options:
 -u,--user    - Your github username
 -t,--token   - Your personal API token obtained from https://github.com/account/admin
 -r,--repo, --repository  The github repository you wish to interact with

Simple Commands:
 tags          - List labels used by the project
 list          - List all the project's open bugs
 start         - Start working on the listed issue(s), sets a label called 'In Progress'
 close         - Close the listed issue(s), unsets the 'In Progress' label
 clone-rhel    - Clone the specified issue(s) to a bugzilla for RHEL 6
 clone-fedora  - Clone the specified issue(s) to a bugzilla for Fedora 15

Contextual Commands:
 b,bugs        - Label issues with 'Bug', or list existing issues with that label if no issues are specified
 f,features    - Label issues with 'Feature', or list existing issues with that label if no issues are specified
 t,tag text    - Apply the specified label to specified issue(s), or list issues with that label otherwise
                 May be specified multiple times
 u,untag text  - Remove the specified label from specified issue(s)
                 May be specified multiple times

Example usage:
 alias g='github-issue -u beekhof -t your_github_api_token -r ClusterLabs/pacemaker'

 g                       # List all open issues
 g bugs                  # List all open Bugs
 g show 1                # Show details of issue 1
 g tag 'My Label' 1 3    # Add 'My Label' to issues 1 and 3
 g tag 'My Label'        # Shows all issues tagged with 'My Label'
 g untag 'Your Label' 3  # Remove 'My Label' from issue 3
```
