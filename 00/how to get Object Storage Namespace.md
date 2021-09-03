# How to get the Object Storage Namespace in the OCI admin web console.
Object Storage, namespace serves as the top-level container for all buckets and objects. At account creation time, each Oracle Cloud Infrastructure tenant is assigned one unique system-generated and immutable Object Storage namespace name. For more information about Object Storage Namespace please click [here](https://docs.oracle.com/en-us/iaas/Content/Object/Tasks/understandingnamespaces.htm).

You can get you tenancy *Object Storage Namespace* from several ways in OCI. Using the oci cli running next console command:
```sh
oci os ns get
```
Your Object Storage Namespace will be returned in json format as:
```json
{
    "data": "MyNamespace"
}
``` 
And of course with the web console. You must login in the OCI web console with your credentials. Then click in your profile icon (top right) and select **Tenancy:*<your_tenancy_name>***

![](./images/oci-obnamespace-01.png)

Your namespace string is listed under **Object Storage Settings**.

![](./images/oci-obnamespace-02.png)
