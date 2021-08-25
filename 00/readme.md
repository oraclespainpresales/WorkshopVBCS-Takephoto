# Visual Builder workshop.
This workshop will teach you how to create a new Oracle Visual Builder mobile application, that will allow you to take a photo with the mobile camera and upload it to Oracle Cloud (OCI) Object Storage.

<details>
  <summary>1.- Creating the API Key.</summary>

---
You will have to connecto the Visual Builder app to OCI Object Storage Bucket to Store the mobile photo or image files. You must create an API key OCI element to access to the OCI Services via API REST. Let's create the API Key.
  
---
  
## Creating the API Key
First Sign in [OCI web console](https://cloud.oracle.com) with your credentials 
> Note: this credentials will be provided to you in the workshop by the trainers, or you can use youw own credentials if you have a trial or paid tenancy.

Write your tenancy name and click **Next** Button.

![](./images/oci-signin-01.png)

Then click Continue leaving the Identity Providers as *oracleidentitycloudservice*

![](./images/oci-signin-02.png)

Next write you *User Name* and *Password* and click in **Connect** Button to access to OCI web console.

![](./images/oci-signin-03.png)

![](./images/oci-signin-04.png)

Then click in the **Profile icon** at the top right of the console to access to the user **Settings**.

![](./images/oci-apikey-01.png)

Scroll down and click **API Keys** in the *Resources menu*

![](./images/oci-apikey-02.png)

Next click **Add API Key** button to add a new API Key.

![](./images/oci-apikey-03.png)

Select **Generate API Key Pair**. 
> Note: you could use your own public and private keys in pem format, but in this workshop and for academical purposes we'll use the auto generathed keys.

![](./images/oci-apikey-04.png)

Next you must to download the *Private* and *Public* Keys to your laptop/desktop.

![](./images/oci-apikey-05.png)

After that, you might have two **.pem** files one mark as public.

![](./images/oci-apikey-06.png)

Then click in **Add** button.

![](./images/oci-apikey-07.png)

Next window is the summary or **Configuration File Preview**. Click in the **copy** link to copy your OCI API credentials to a text file in you local computer as you will need them in future steps in the workshop. Then click **Close** Button to finish the process.

![](./images/oci-apikey-08.png)

You might have a new API key created and you should see the Fingerprint key in the OCI web console. 

![](./images/oci-apikey-09.png)

You can get the Config file that you copied before clicking in the *tree vertical* dots in the Fingerprint row and select **View Config File**.

![](./images/oci-apikey-10.png)
</details>
<details>
  <summary>2.- Acessing Visual Builder Studio and WorkSpace using Visual Builder Cloud Service</summary>
  
---
  To develop your Visual Builder Application you must access to the workshop Visual Builder Studio instance. Visual Builder is not only used to develop Visual Builder applications, but it allows the development of any kind of modern application thanks to its multitude of integrated development tools, such as a GIT repository, CI/CD pipelines engine, artifact generation, container repository, agile tools, team building tools like wiki and snipples and more. If you want to know more please click [here](https://www.oracle.com/application-development/visual-builder-studio/)
 
---
  
## Acessing Visual Builder Studio and WorkSpace using Visual Builder Cloud Service
To get access to Visual Builder Studio (VBS) you have to Sign-in Oracle Cloud web console with your tenancy user credentials. Then Click in the *hamburguer icon* in the top left part of the web console and select **OCI Classic Services** then click in **Developer** to access to Visual Builder Studio instance.

![](./images/oci-vbs-01.png)
  
Next you have to click in the VBS instance **menu icon** and click in the **Access Service Instance**
  
![](./images/oci-vbs-02.png)  
 
Then in **Organization**, select the *Project* -> **Workshop-VBCS-Takephoto** that you will use for this workshop. 
  
![](./images/oci-vbs-03.png)
  
Select *Workspaces* in the left menu to get all the workspaces in the project. Then select the appropiate workspace asigned to you by the trainer. In this tutorial, you will see that the screenshots show *userXX*, but you will have to change XX with your user number.
> Note: if the trainer asign you the numbre 01 or user01, your workspace will be something like **workspace-user01**.
  
All trainees will use their own git repository tied to their own workspace.
  
![](./images/oci-vbs-04.png)
  
Wait a couple of second to access to your workspace. You should see the *Welcome to your Workspace* page.
  
![](./images/oci-vbs-05.png)
    
</details>
</details>
<details>
  <summary>3.- Creating a Mobile App in Visual Builder.</summary>
  
---
In this section you will create a mobile application with Visual Builder low coding programing. This application will have several components like an API REST connection to Oracle Cloud Object Storage bucket to storage your photos or files, a mobile layout with input fields and button to take the photo, a workflow triggered by the button event handler and more. At the end of the section you will can take a photo with you mobile phone and upload it to an OCI Object Stogare bucket.
 
---
  
## Creating a Mobile App in Visual Builder.
In Visual Builder you can create web applications as well as mobile applications. As a low coding programing platform you have a lot of preconfigured UI components to create an application layout for you business case. But you can use javascript (nodejs notation) if you want to have more control over your application. The limit is your imagination.

<details>
  <summary>3.1 Creating the mobile layout</summary>
  
### Creating the mobile layout.
Now you will create the mobile layout adding several components that you will use and combine in future sections to create the mobile application.
  
Click in the mobile left menu icon and then click **+ Mobile Application** button to create a mobile application.
  
![](./images/vbs-app-01.png)
  
In *General Information* you must to write a descriptive name for your mobile app, like **takephotoapp**. Then select none as mobile layout app, because in this workshop we won't create a navigation menu for the app as it has only one screen. Finally click **Next** button to continue.
  
![](./images/vbs-app-02.png)
  
Keep **Custom** layout selected (empty layout) and click **Create** button to create you mobile app.
  
![](./images/vbs-app-03.png)

Now you should have created the visual builder mobile application environtment/sandbox to continue creating your mobile app. You should see the *Page Designer* selected with a simple mobile layout in the Design window.
  
![](./images/vbs-app-04.png)
  
You can change the mobile appearance (iphone, google pixel, samsung or tablet), show or hide the bezel or change the mobiile size. In the tutorial we select Samsung Galaxy S20 layout, but you can select whatever you want (default layout is for iphone mobile phones).
  
![](./images/vbs-app-05.png)
  
Click in **Page Title** to select the *Mobile Page Template* properties. Then change the page title to a descriptive one like **Take a Photo to OCI App**
  
![](./images/vbs-app-06.png)
  
Select **Flex Container** layout to change it.
  
![](./images/vbs-app-07.png)
  
Change the *Display Settings* to **Grid** layout.
  
![](./images/vbs-app-08.png)
  
Scroll down in the Components menu to Layout and drag and drop **Form Layout** to the Design window.
  
![](./images/vbs-app-09.gif)
  
Scroll up or search an **Input Text** component and drag and drop to the Design window, inside the *Form Layout*.
  
![](./images/vbs-app-10.gif)
  
Now you will add other **Input Text** but you'll drop it in the Structure menu instead of drop it over the Design window. Drag and Drop over the Structure menu gives you more control when you are creating the mobile layout.
  
![](./images/vbs-app-11.gif)
  
Next you will add a **Horizontal Rule** from *Layout* components to the Design window.
  
![](./images/vbs-app-12.png)
  
Now you have to scroll down and add an **If** component from *Layout* menu to the Structure tree. 
> Note: This component will allow you to compose match rules to create different behaviours according to that rules. In this workshop you will use the **If** component to show or hide the *take photo button*, that you'll have to add to the Design window in next steps.
  
![](./images/vbs-app-13.gif)
  
Add other **If** component more to the *Structure tree*, but this time you have to add it inside (nested) the last *If* that you created before.
> Note: You have to create two nested if components, one for each **Input Text** added before.

![](./images/vbs-app-14.gif)
  
Next you have to add a **Grid Container** component from *Layout* menu, nested to the last *if* component in the *Structure* tree. Drag the **Grid Container** component and drop it inside the last **Bind If**.
> Note: The Grid Container (show as *Grid Row* in the Structure tree) will contain the next components that you have to crete and you'll use it to show or hide its content according to the match rules that you will create in the *If* components in future steps.
  
![](./images/vbs-app-15.png)
  
Now you have to add a **Camera** Component from *Commom* menu, nested to the Grid Row that you create in the last step.
> Note: The Camera component is made up of three components: a **File Picker** and a **Button** with an **Icon**. The File Picker component will have a special behaviour as the action that it will execute, will be triggered by the button instead of the own File Picker component.
  
![](./images/vbs-app-16.gif)
  
Next add other **Horizontal Rule** component from *Layout* components menu as a separator. You must drag the **Horizontal Rule** and drop inside the **Camera** component in the *Structure* tree.
  
![](./images/vbs-app-17.gif)
  
Last Layout component will be an **Image** one. Drag the **Image** component from the *Common* components menu and Drop inside the **Grid Row**. **Image** component should be at the same level as the **Camera** component.
  
![](./images/vbs-app-18.gif)

Now you should have a Structure tree similar the next screenshot. You can move components in the structure tree if your layout structure is different.
  
![](./images/vbs-app-19.png)
  
</details>
<details>
  <summary>3.1 Configuring the components created</summary>
  
  
</details>
</details>
