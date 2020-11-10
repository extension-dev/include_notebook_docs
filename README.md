# include.ai Notebook Documentation
Welcome to include!

The [include.ai](http://include.ai/) Notebook is a web-based interactive Notebook that can be published to hide code and data flow complexity. When published, the include.ai Notebook becomes a simple linear application that blends text (explanations) and actions (user interactions, code).

### What is a Notebook?
Here's a quick mental model: you can think of the include.ai Notebook as the "micro-service architecture" take on internal tools. **Each Notebook accomplishes a single task** (remove/add a user, change a feature flag, upload a CSV to a user's demo account)**.** Because each Notebook solves only one task, it is faster to develop and easier to use, maintain, and share than apps built with traditional UI app builders.

Developing in include.ai is similar to the iterative and interactive development in Jupyter notebooks. Each Block in an include.ai Notebook runs independently and returned data is accessible in later blocks. Similar to other Notebooks, you can do cool things like calling a slow API once to grab user data and then run multiple code blocks to clean/process the data without rerunning the API.

In addition to the basic text and code Blocks, the include.ai Notebook also includes user-interaction Blocks (input, dropdown, CSV upload) and visualization Blocks (template string replacing in Markdown, Table). More Blocks are being added every day (let us know what blocks you want)! For more documentation on Blocks, see the Blocks section.

All of our features are focused on reducing the friction to build and use Notebooks. Try it for yourself; you can create and publish a new Notebook in less time than it takes to decide on a front-end framework to use.

### What is it good for? 

The include.ai Notebook excels at self-contained tasks that "do something." These tasks usually take user input (text input, dropdown, uploading a file), call product APIs, run SQL queries, or run Javascript. Typical use cases are: removing/adding a user, changing feature flags, joining multiple CSVs with SQL, enriching CSVs with APIs, and uploading CSVs into users' demo accounts.

### What is it not good for? (When should you not use include.ai?)

include.ai Notebooks are not ideal for complex internal tools that resemble a database (check out Airtable or Retool) or for highly interactive data science apps (check out StreamLit). If you are writing an interactive essay with a focus on visualization, check out Observable. If you do not need to publish your Notebook as an app, stick with Jupyter or Google Colab.

# Notebook Basics

## Building a Notebook
An include.ai Notebook is an interactive web notebook that allows you to build simple apps with inputs, data visualization, and raw code. You can also easily hide away all the complexity to transform your notebook into a simple linear application that anyone can use.

### Blocks

![Create Blocks](images/1-new-block.png)

Each include.ai Notebook is made up of a linear series of "Blocks." They are the atomic unit of the include.ai Notebook ecosystem. There are a few different types of blocks:

**Display Blocks** display well-formatted data such as text and tables:
   
* Text Block
* Table Block

**Interaction Blocks** allows users of the notebook to input data or control certain variables:

* Input Block
* CSV Block
* Dropdown Block

**Command Blocks** are used to execute certain functions like custom-defined javascript, API calls, or even SQL queries:
* Code Block
* SQL Block

Check out the Block Reference section and Block Basics for the full documentation.


### Publishing Notebook into Mini-apps
One key feature of an include.ai Notebook is in "publishing." Upon publishing, the Notebook automatically hides away a lot of the complexity, such as raw javascript code and SQL instructions. The notebook becomes a simple-to-read, self-explanatory mini-app that anyone can use.

![Publish Notebook](images/2-publish-setting.png)


## Workspaces, Sharing, and Publishing to the World

### Why Workspaces?

Notebooks aren't very useful by themselves. They shine in a collaborative work environment: when you're making a notebook for a team member or what to use a notebook created by your team.

Introducing the Workspace concept: It is a way to organize your notebooks -- note only for yourself but also for the rest of your team. With workspaces, you have fine-grained control over not only who gets to see your notebooks but also who can make edits and publish them.

Everyone starts with a personal workspace that is private to themself. You can always create workspaces and invite your colleagues through email. Click on the three dots next to the workspace name.

![Modify Workspace](images/3-workspace-three-dots.png)

And then type in your collaborator's email and the corresponding permission you want to assign to them.

![Add Collaborators](images/4-add-collaborators.png)

### Access Control through Workspaces

There are three levels of permission for each workspace: Owner, Editor, and Viewer.

* **Owner**: the creator of the workspace and automatically have access to edit the notebooks
* **Editor**: can also edit the notebook and use published notebooks
* **Viewer**: can only use published notebooks within a workspace.

Differentiated access privilege across different workspaces allow you to securely deliver what the Notebook needs to accomplish by only exposing parts of your larger tooling environment.

### Configuring Resources and Environment Variables for Workspaces

Each Workspace also comes with configurable environment variables and resources. These environment variables can include sensitive data like API keys or common configuration setups repeated across notebooks. Resources are integrations into your systems like your Postgres database.

Configure these variables and resources by first clicking on the three dots next to the workspace name. And then navigate to the "Environment Variables" or "Database" tab.

![Environment Variables](images/5-env-vars-setting.png)

### Publish your Notebook to the World

Sometimes, you may want more than just your team to see your work. With include.ai Notebook, you can quickly publish your notebook to the rest of the world. So anyone with a shared link can visit use your published notebook.

To publish your notebook, click on the top right corner of a Notebook and then click on "Share with the world."

![Public Notebook](images/6-public-notebook-menu.png)

One security tip: making your notebook public potentially exposes all of your code to the open world. Make sure you don't include any sensitive information like API keys in your notebook. Instead, use environment variables in API calls to protect your keys.


