# New Project SOP

Follow these steps whenever you start a new development project. Ideally, update these SOPs to fit your exact workflow. This will allow you to have a consistent workflow for all the projects you work on, saving you lots of time in the long run.

  

### Workflow

1. Create main project folder based on template → `Projects/Client - Project Name`
2. Move proposal from `Areas/Proposals` → `Projects/Client - Project Name/01 Documents`
3. Move any other project information (that doesn't belong in the repo) to this folder
4. Create a new repository from a [template repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
    1. Use the [general project template](https://github.com/daveebbelaar/df-general-project-template)
    2. Use the [data science project template](https://github.com/daveebbelaar/df-data-science-template)
    3. Create your or use your own template
5. Select the owner, repo name, and set it to private
    1. For the repo name I recommend following: `client-project-description` → For example: `asml-slackbot-backend`
6. Clone the repository to your repository folder
7. Open it in your IDE of choice and save it into a project (e.g., VS Code workspace file)
8. Add all the relevant information to the repository (e.g., data, API keys, docs)
9. Store API keys and others credentials in 1Password (optional)
10. Create a new environment (e.g., `Conda` or `venv`) and install dependencies (optional)
11. Create a new project in project management tool (e.g., ClickUp, Linear, Jira, Trello)
    1. For ClickUp, create a new project in `Space → Projects → Client - Project Name` using the [development project template](http://clickup.pxf.io/0ZDazJ)
12. Configure your project and add any automations and/or GitHub integrations
13. Fill the board with your initial features and add clarification where needed
14. Add team members to the repositories and kanban boards (optional)
15. Create a Slack communication channel for collaboration (optional)
    1. Channel name: `client-project-name`
16. To start working on features, copy the branch name from your Kanban board, check out the new branch, complete the feature, and push all the changes to your branch. Then, create a PR (Pull Request) to your main branch to merge everything. Ensure there are no conflicts and merge the request, completing the feature. Finally, delete both the local and remote branch to clean everything up. Now you can continue with the next feature, following a similar workflow.