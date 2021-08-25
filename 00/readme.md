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
  <summary>2.- Acessing VBCS and WorkSpace</summary>
  
---
  To develop your Visual Builder Application you must access to the workshop Visual Builder Studio instance. Visual Builder is not only used to develop Visual Builder applications, but it allows the development of any kind of modern application thanks to its multitude of integrated development tools, such as a GIT, CI/CD pipelines engine, artifact generation, container repository, agile tools, wiki, snipples and more. If you want to know more please click [here](https://www.oracle.com/application-development/visual-builder-studio/)
 
---
  

</details>
