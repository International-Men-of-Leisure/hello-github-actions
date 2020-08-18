
## What are Github Actions?

GitHub Actions are a flexible way to automate nearly every aspect of your team&#39;s software workflow. Here are just a few of the ways teams are using GitHub Actions:

- Automated testing (CI)
- Continuous delivery and deployment
- Responding to workflow triggers using issues, @ mentions, labels, and more
- Triggering code reviews
- Managing branches
- Triaging issues and pull requests

Actions can be used from within the same repository, from any other public repository, or from a published Docker container image.

## Types of Actions

Actions come in two types: container actions and JavaScript actions.

Docker container actions allow the environment to be packaged with the GitHub Actions code and can only execute in the GitHub-Hosted Linux environment.

JavaScript actions decouple the GitHub Actions code from the environment allowing faster execution but accepting greater dependency management responsibility.

## Setup Steps

1. **Add a Docker File**
* Actions will be executed in an environment defined by this file.
* The entrypoint.sh script will be run in Docker, and it will define what the action is really going to be doing.
2. **Add an Entry Point Script**
3. **Add an Action File**
* All actions require a metadata file that uses YAML syntax. The data in the metadata file defines the inputs, outputs and main entrypoint for your action.
4. **Add a Workflow File**
* Workflows are defined in special files in the .github/workflows directory, named main.yml.
* Workflows can execute based on your chosen event, for example upon pushing to the repo.

## What is a Workflow?

Workflows piece together jobs, and jobs piece together steps, and together these define the actions we want to run.

- jobs: is the base component of a workflow run
- build: is the identifier we&#39;re attaching to this job
- name: is the name of the job, this is displayed on GitHub when the workflow is running
- steps: the linear sequence of operations that make up a job
- uses: actions/checkout@v1uses a community action called [checkout](https://github.com/actions/checkout) to allow the workflow to access the contents of the repository
- uses: ./action-a provides the relative path the action we&#39;ve created in the action-adirectory of the repository
- with: is used to specify the input variables that will be available to your action in the runtime environment. In this case, the input variable is MY\_NAME, and it is currently initialized to &quot;Alex&quot;.
## Additional Info

-   You can follow the tutorial [here](https://lab.github.com/githubtraining/github-actions:-hello-world) to learn more about using Github Actions!

-   Checkout the [Github Actions marketplace](https://github.com/marketplace?type=actions) to find all kinds of Github Actions for your projects!
T
