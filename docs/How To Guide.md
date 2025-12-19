# Install Python using installer

1. Pre-requistes
Create a folder c:\utils
> Note: All installations to be done in this folder and NOT in the default Windows folder

2. Go to the official Python downloads page for Windows: https://python.org/downloads/windows/.

3. Download the latest stable version by clicking "Windows installer (64-bit)" or the appropriate option for your system.

4. Locate the downloaded .exe file and run it to start the installation wizard.

5. In the installer window, check the box that says Add python.exe to PATH.
Note: This is a crucial step for running Python from the command line.

6. Choose Customize installation.

7. On the Optional Features page, remove the Option "for all users (requires admin privileges)", if you do not have admin privileges.

8. In the Advanced Options page, in the Customize install location, change the install location to the folder created earlier.
Note: if the default path specified is
C:\Users\Akash.Rajput\AppData\Local\Programs\Python\Python313
change to
C:\utils\Python313 i.e. Install python in a folder inside c:\utils

9. Select Install.

10. Click Close once the installation is complete.

# Installing MkDocs Material

To install **MkDocs Material** using Python, you will use `pip`, Python's package installer. Ensure **Python** and **pip** are installed.

---

1. Verify Python and pip Installation

Before installing MkDocs Material, verify that you have **Python** and **pip** installed on your system.  
You can check their versions with the following commands in your terminal:

```bash
python --version
pip --version
```

If they are not installed, you will need to install **Python** first, which typically includes **pip**.

---

2. Install MkDocs Material

Open your terminal or command prompt and execute the following command:

```bash
pip install mkdocs-material
```

This command will download and install the **MkDocs Material** theme and its dependencies.

---

3. Create a New MkDocs Project

If you are starting a new documentation project, create a new MkDocs project with:

```bash
mkdocs new my-project
cd my-project
```

---

4. Configure the Material Theme

Open the `mkdocs.yml` file in your project directory and add or modify the theme setting to use Material:

```yml
theme:
  name: material

features:
    - navigation.tabs #For nav bar at top header

nav:
	- Home: index.md
	- U2C Designs:
		- U2C Designs/index.md
		- Mobility: mobiloity.md
```

5. Serve Your Documentation

Navigate to your project directory in the terminal and run the MkDocs development server to preview your site with the Material theme:

```bash
mkdocs serve
```

You can then access your documentation in a web browser, typically at:

👉 [http://localhost:8000](http://localhost:8000)

---

6. Virtual Environment

- Create a Virtual environment

> Type ```python -m venv mkdocs-env``` and press Enter.

- Activate Virtual environment

> Type ```.\mkdocs-env\Scripts\activate``` and press Enter.

---

# Installing MERMAID for flowchart rendering

1. Open command prompt and navigate to the python installation folder  
- Run following Commands
```
	pip install mermaid-py
	pip install mkdocs-mermaid2-plugin

```
- If you get error run these as well
```
	pip install mermaid-cli 
	playwright install chromium
```
2. Add the below code in the yml file
```yml
markdown_extensions:
  - pymdownx.superfences: #for flowchart renders
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
```

To know..How to create flowcharts, Squence Diagrams in Mermaid [Click Here](https://docs.mermaidchart.com/mermaid-oss/syntax/flowchart.html#a-node-rhombus)

# Going Live on Git

1. create a new repository on the command line

```bash
echo "# U2C-Documentation-Portal" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/AkashRajputHUB/U2C-Documentation-Portal.git
git push -u origin main

```
2. push an existing repository from the command line

```bash
git remote add origin https://github.com/AkashRajputHUB/U2C-Documentation-Portal.git
git branch -M main
git push -u origin main
```

3. Process for github page (via tutorial)

```bash
git init  #to initiate the local git repository
git add . #to add all the files in git repository
git status #to check the file status
git commit -m 'Initial commit' #to commit 

now, go on gitbug create a new repository and copy the below remote details`

git remote add origin https://github.com/AkashRajputHUB/U2C-Documentation-Portal.git (get this from the github once we create repository there)
git branch -M main
git push -u origin main
```

4. Update the live github pages

```bash
git add .
git status
git commit -m "Descriptive message about your updates"
git push -u origin main
```

# For Markdown Syntax

[Markdown syntax Guide](https://www.markdownguide.org/)

- This is example of _italic text_
  >eg: ```This is example of _italic text_```

- This is the **BOLD text**
  > eg:``This is the **BOLD text** in the IOT sample feature``

- <mark>This is the HTML tag example for highlighted text in mkdocs</mark>
  >eg: ``<mark>This is the HTML tag example for highlighted text in mkdocs</mark>``

- <s>This one is the example of the striked text via ```<s>``` parameter in IOT sample feature</s>
  >eg: ``<s>This one is the example of the striked text via ```<s>``` parameter in IOT sample feature</s>``

- <del>This one is the example of the striked text via ```<del>``` parameter in IOT sample feature</del>
  > eg: ``<del>This one is the example of the striked text via ```<del>``` parameter in IOT sample feature</del>``

- This is an example of creating hyperlink within the site pages [click here for useful links](useful links.md)
> `[click here for useful links](useful links.md)`

- This is an example of hyperlink [Jio.com](https://Jio.com)
> `[Jio.com](https://Jio.com)`

- Making section header as clickable:  
`[Click Here for mermaid guide](#installing-mermaid-for-flowchart-rendering)` <!-- Keep the section header name in all small letter and keeping - berween each word-->  

Example: [Click Here for mermaid guide](#installing-mermaid-for-flowchart-rendering)

- Marking Comment in markdown
`<!-- This is a comment example -->`  write the text in between `<!-- text -->`  
Example: If you can't see the exmaple then it's working fine ;)  
<!-- Keep the section header name in all small letter and keeping - berween each word-->  

- This is an example of table :

  |Test|Test|Test|
  |---|---|---|
  |123|456|678|
  

>eg: ```|Test|Test|Test|``` ```table header```

  ```|---|---|---|``` ```for new line```

  ```|123|456|678|```   ```content```

> [!NOTE]  
> Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]  
> Crucial information necessary for users to succeed.

> [!WARNING]  
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.


- Adding image in the  markdown  
`![alt text](Isolated.png "Title")`


- Example : `![Jio](assets/Jio.png "Jio Logo")`

![Jio](assets/Jio.png "Jio Logo")

---

# My Sample YAML file

```yml
site_name: Documentation Portal Sample Site   
markdown_extensions:
  - pymdownx.superfences: #for flowchart renders
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
nav:
      - Home: index.md
      - Line of Business: 
        - U2C Designs/index.md
        - Mobility:
          - U2C Designs/Mobility/index.md
          - Feature Example: sample.md
        - Home:
          - Fiber: 
            - Feature 1234: Fiber feature sample.md
        - IOT:
          - Feature ABC: IOT feature sample.md
      - Mkdocs & Markdown Guide: How To Guide.md
      - Flow charts: diagram.md
      - About: About.md
   
theme:
    name: material
    logo: assets/Jiologored.png
    favicon: assets/Jio.png
    palette:
        primary: blue gray
        accent: red
    features:
    #- navigation.tabs #for navigation options at top header
    - navigation.tabs.sticky # to prevent nav hiding
    - navigation.path #to show the navigation paths
    #- navigation.sections #to group the left panel sections
    - toc.integrate #integrate table of content in nav panel
    - toc.follow #to keep the left pan follow the content on .md data 
    - navigation.top #for back to top button
    - navigation.instant
    - navigation.instant.prefetch #to preload the pages when user howers the link
    - navigation.instant.progress #for loading bar/ring
    - navigation.indexes #to have the index pages for each sub section in the nav panel
    #- Search.highlight #to highlight searched content on md pages

```