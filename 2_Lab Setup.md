# Getting Started with Amazon Bedrock and Prompt Engineering

**Oct. 23, 2025 - Oct. 31, 2025**  
**Machine Learning University**

## Amazon Bedrock

A fully-managed service that makes foundation models available via an API

Foundational Models available:
* Amazon (Titan)
* A121Labs (Jurassic-2)
* Anthropic (Claude)
* cohere (Command)
* stability.ai (Stable Diffusion)
* CompanyName (Model Name)

## Amazon SageMaker Studio Lab with Amazon Bedrock

This page lets you access a temporary AWS account with an Amazon SageMaker Studio environment with access to Amazon Bedrock models where you can run your MLU course's lab.

## Starting Your Lab

1. In the top-right corner of this page, choose the **Start Lab** button.
2. The message "Your lab is provisioning, please wait..." appears. This process may take up to 15 minutes to complete.
3. When the lab creation process finishes, two buttons appear.
4. Click on the **AWS** button, which automatically logs you into the AWS Management Console in a new tab.
5. In the top-right corner of the AWS Management Console, check that the Federated user starts with `AWSLabsUser` to confirm that you are logged into the MLU-provided AWS Labs account.
6. To the left of the Federated user, check that the selected AWS region is **United States (N. Virginia)**. For any region other than United States (N. Virginia), open the dropdown and select **N. Virginia us-east-1** from the list.

> **Note:** Depending on your actions in the AWS Management Console, red error boxes may appear. Generally, unless these messages prevent you from following the steps below, they can be ignored.

## Accessing Amazon SageMaker Studio

1. At the top of the AWS Console, in the search bar, type **Amazon SageMaker AI** and select it from the list of services.
2. In the left navigation panel, under **Applications and IDEs**, choose **Studio**.
3. The Amazon SageMaker Studio landing page loads. A Studio domain has been pre-created in this account. You do not need to create any further resources to run this lab.
4. In the Get Started card, make sure that **mlulearner** is selected as user profile, and click on **Open Studio**.
5. A new tab will open to display the Amazon SageMaker Studio console. If a pop-up appears asking you to take a SageMaker Studio tour, you may choose **Skip Tour** for now.
6. In the left navigation panel, in the **Applications** section, choose **JupyterLab**.
7. A table listing JupyterLab spaces is displayed. A space named **MLUJupyterLabSpace** has been pre-created for you.
8. If the Status of the space is **Stopped**, then in the Action column, click **Run**.
   - Starting a space may take up to 10 minutes.
9. If the Status of the space is **Running**, then in the Action column, click **Open**.
10. A new tab opens running JupyterLab.

> **Note:** To be frugal, spaces are automatically stopped if they are idle for four hours.

To complete the lab activities you will need to upload the lab materials found on the course content page to JupyterLab.

## Uploading Your Lab Content

1. Your MLU course content page contains a link to download the course's lab. You can navigate to your course content page from MY-MLU by clicking on the course's name.
2. Locate the lab zip file in the course content page and download it to your local machine.
3. In JupyterLab, to upload the zip file, below the menu bar choose the arrow-shaped upload icon, select the zip file in your local machine, and confirm by choosing **Open**. Alternatively, you can drag and drop the zip file from your local machine onto the JupyterLab left sidebar.
4. In JupyterLab, select **File > New > Terminal** to open a new tab with a terminal prompt.
5. In the terminal window, copy and paste the command below, replacing `<course_lab>` with the actual name of the zip file.

```bash
unzip <course_lab>.zip; rm <course_lab>.zip
```

6. In the JupyterLab left sidebar find a new, unzipped folder containing the materials for your lab. Double-click on the folder name to access its contents. The lab notebooks have extension `.ipynb`. When you double-click on a notebook, it opens in a new tab and you can start working on it.

## Resuming or Ending Your Lab

> **Note:** You can resume your lab at any time during your course, but once you end the lab, all content is lost and cannot be restored.

### Resuming Your Lab

- Your lab will last for as long as your MLU course does. Whenever you want to stop working for the day, simply close the JupyterLab browser window.
- To resume your lab, come back to this page and click on the **Start Lab** button. If you get a message indicating that your credentials are expired, click "Log out" at the bottom of the page and click on **Start Lab** again.

### Ending Your Lab

- Your lab will automatically end when your temporary AWS account expires. If you want to end the lab earlier, click on the **End Lab** button. Be aware that ending your lab will permanently terminate all resources on it.

## Saving Your Work

If you want to save your work, you need to download it to your local machine.

### To download an individual notebook:
- In the JupyterLab left sidebar right-click on the file name and select **Download**.

### To download all course content:

1. Open a new terminal.
2. Install zip in Studio by running the command below in the terminal:

```bash
sudo apt install zip
```

3. Create a zip file with your course materials by running the command below in the terminal (where `<your_folder_name>` is the name of the folder that you want to save):

```bash
zip -r mlu_content_backup.zip <your_folder_name>
```

4. In the JupyterLab left sidebar, right-click on the name of your backup zip file and select **Download**.