# GitHub Teams and Access Control

Managing access to specific repositories in a GitHub organization using Teams is a powerful way to
streamline permissions, reflect your group’s structure, and maintain security. Here’s how you can
do it effectively, based on standard GitHub functionality and best practices:

- **[Understand Teams and Their Role](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams):**
    - In a GitHub organization, Teams are groups of members that can be assigned specific permissions to
     repositories. They allow you to manage access collectively rather than individually, which simplifies
     administration, especially as your organization grows.
    - Teams can mirror your company’s structure (e.g., "Frontend Devs," "QA Team") and support nested
    hierarchies (parent and child teams), where child teams inherit permissions from their parents.
- **[Create Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/creating-a-team):**
    - Go to your organization’s main page on GitHub.
    - Click the Teams tab.
    - Click New team.
    - Give the team a name (e.g., "Backend Team") and an optional description.
    - Choose a parent team if applicable (for inherited permissions).
    - Set the team visibility: "Visible" (all org members can see it) or "Secret" (only team members can see it).
    - Use descriptive names to reflect the team’s purpose or project focus.
- **[Add Members to Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/adding-organization-members-to-a-team):**
    - On the team’s page, go to the Members tab.
    - Click Add a member.
    - Search for organization members by username or email and add them.
    - You can also assign the "Team Maintainer" role to specific members, allowing them to manage the team (e.g., add/remove members, adjust settings) without needing full admin rights.
    - Note: Only organization members can be added to teams; outside collaborators are managed separately.
- **[Assign Teams to Repositories](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository):**
    - Navigate to the repository you want to manage.
    - Click Settings (you’ll need admin access to the repo).
    - In the sidebar, select Collaborators and teams.
    - Under "Manage access," click Add teams.
    - Search for the team name and select it.
    - Choose a permission level (see below).
- **[Permission Levels](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization):**
    - Read: View and discuss the repo (good for auditors or non-contributors).
    - Triage: Manage issues and pull requests without write access.
    - Write: Push code and contribute directly.
    - Maintain: Manage repo settings and branches without sensitive actions (e.g., deleting the repo).
    - Admin: Full control, including destructive actions and security settings.
