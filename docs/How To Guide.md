# Installing MkDocs Material

To install **MkDocs Material** using Python, you will use `pip`, Python's package installer. Ensure **Python** and **pip** are installed.

---

## 1. Verify Python and pip Installation

Before installing MkDocs Material, verify that you have **Python** and **pip** installed on your system.  
You can check their versions with the following commands in your terminal:

```bash
python --version
pip --version
```

If they are not installed, you will need to install **Python** first, which typically includes **pip**.

---

## 2. Install MkDocs Material

Open your terminal or command prompt and execute the following command:

```bash
pip install mkdocs-material
```

This command will download and install the **MkDocs Material** theme and its dependencies.

---

## 3. Create a New MkDocs Project

If you are starting a new documentation project, create a new MkDocs project with:

```bash
mkdocs new my-project
cd my-project
```

---

## 4. Configure the Material Theme

Open the `mkdocs.yml` file in your project directory and add or modify the theme setting to use Material:

```yaml
theme:
  name: material
```

---

## 5. Serve Your Documentation

Navigate to your project directory in the terminal and run the MkDocs development server to preview your site with the Material theme:

```bash
mkdocs serve
```

You can then access your documentation in a web browser, typically at:

👉 [http://localhost:8000](http://localhost:8000)

👉 [Puneet Sir's Guide](http://docs.jio.com/integration-arch/faq/)

---

## 6. Virtual Environment

- Create a Virtual environment

> Type ```python -m venv mkdocs-env``` and press Enter.

- Activate Virtual environment

> Type ```.\mkdocs-env\Scripts\activate``` and press Enter.

---


## 7. Text commands in markdown

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


- This is an example of table :

  |Test|Test|Test|
  |---|---|---|
  |123|456|678|
  

>eg: ```|Test|Test|Test|``` ```table header```

  ```|---|---|---|``` ```for new line```

  ```|123|456|678|```   ```content```us