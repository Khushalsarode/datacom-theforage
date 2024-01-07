# GitHub Actions Demo

This repository serves as a demonstration of GitHub Actions and showcases the utilization of variables within the repository settings.

## Workflow: Explore-GitHub-Actions

The workflow defined in the `.github/workflows/main.yml` file is named `Explore-GitHub-Actions`. It is triggered on every push event and runs on the latest version of Ubuntu. The workflow consists of the following steps:

1. **Print Event Information:** Displays information about the triggering event, including event name and the type of server hosting the job.

2. **Check out Repository Code:** Uses the `actions/checkout` action to clone the repository code onto the GitHub Actions runner.

3. **Display Repository Information:** Prints details about the repository, such as the branch name and repository name.

4. **List Files in the Repository:** Lists the files in the cloned repository on the GitHub Actions runner.

5. **Display Job Status:** Prints the status of the current job.

### Variable Usage

- `${{ github.actor }}`: Represents the user or the GitHub App that initiated the workflow.
- `${{ github.event_name }}`: Holds the name of the event that triggered the workflow (in this case, a push event).
- `${{ runner.os }}`: Specifies the operating system of the runner hosting the job.
- `${{ github.ref }}`: Indicates the name of the branch.
- `${{ github.repository }}`: Refers to the name of the repository.
- `${{ github.workspace }}`: Points to the path where the repository has been cloned on the runner.
- `${{ job.status }}`: Reflects the status of the current job.

