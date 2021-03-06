---
layout: docs
title: Linking your projects
description: Linking your projects
keywords: project actions, attach, build, disable, enable, validate, refresh, link, linking your projects, VS Code, Eclipse
duration: 1 minute
permalink: linking-your-projects.html
type: document
---

# Linking your projects

You can link your projects when you are using Codewind. This feature is available in the [VS Code](#linking-your-projects-in-vs-code) and [Eclipse](#linking-your-projects-in-eclipse) IDEs. Project linking is supported by all Codewind project types and extensions except for the ODO Devfile extension.

For example, use this feature to link a front-end Node.js project to a back-end database. You have a web page front-end Node.js project without a link:

![Image of unlinked project](images/linking-feature/unlinked_project.png){:width="650px"}

You then link it to a back-end Node.js database project:

![Image of linked project](images/linking-feature/linked_project.png){:width="650px"}

## Linking your projects in VS Code

To link your projects in VS Code, follow these steps where project `frontend-nodejs` is the source project and project `database-nodejs` is the target project. Both projects must be running to create a link.

1\. Right-click project `frontend-nodejs` in the **Codewind** view, select **Project Overview**, and then select the **Links** tab.

2\. Click **Create Link**:

![Image of managing VS Code project links](images/linking-feature/vscode_add_project_link.png){:width="650px"}

3\. Select the target project and press **Enter**. 

![Image of selecting VS Code target project](images/linking-feature/vscode_select_target_project.png){:width="650px"}

4\. Enter a name for the environment variable and press **Enter**:

![Image of entering VS Code environment variable](images/linking-feature/vscode_enter_environment_variable.png){:width="650px"}

5\. The link is created and is shown in the **Project Links** section of the **Project Overview**:

![Image of VS Code project links section](images/linking-feature/vscode_manage_project_links_step_4.png){:width="650px"}

6\. Use the environment variable in your code as needed, for example:

```
axios.get(`http://$DATABASE/api/v1/populations`);
```

Where `DATABASE` is the name of the environment variable that you added in step 4. 

7\. If you choose to remove the target project of a link, the **Remove Projects** dialog reminds you that if you remove the project, the link is also removed. If the source project for a link is removed, the link is also removed.

![Image of removing projects](images/linking-feature/vscode_remove_projects.png){:width="650px"}

## Linking your projects in Eclipse

To link your projects in Eclipse, follow these steps where project `frontend-nodejs` is the source project and project `database-nodejs` is the target project. Both projects must be running to create a link.

1\. Right-click project `frontend-nodejs` in the **Codewind Explorer** view and select **Manage Project Links**.

2\. Click **Add**:

![Image of managing Eclipse project links](images/linking-feature/eclipse_manage_project_links.png){:height="550px" width="650px"}

3\. Select the target project, enter a name for the **Environment variable**, and then click **OK**:

![Image of selecting target project](images/linking-feature/eclipse_add_project_link.png){:width="650px"}

4\. The link is displayed in the **Manage Project Links** dialog. Click **OK** to create the link:

![Image of managing links for the front-end project](images/linking-feature/eclipse_manage_project_links_step_4.png){:height="550px" width="650px"}

5\. Use the environment variable in your code as needed, for example:

```
axios.get(`http://$DATABASE/api/v1/populations`);
```

Where `DATABASE` is the name of the environment variable that you added in step 3. 

6\. For convenience, project links are displayed in the **Project Overview** page:

![Image of Eclipse application overview](images/linking-feature/eclipse_application_overview.png){:width="650px"}

7\. If you choose to remove the target project of a link, the **Remove Projects** dialog reminds you that if you remove the project, the link is also removed. If the source project for a link is removed, the link is also removed.

![Image of removing projects](images/linking-feature/eclipse_remove_projects.png){:width="650px"}
