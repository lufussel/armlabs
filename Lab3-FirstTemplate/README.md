# Lab 3 - First Template



## Create a template file

From **Visual Studio Code (VS Code)**, open a working directory such as `C:\Temp\armlabs`

Create a new folder such as `FirstTemplate`

Create a new file named `azuredeploy.json`. **azuredeploy.json** is the standard naming convention for an ARM template file, however any filename will work successfully. [IntelliSense](https://code.visualstudio.com/docs/editor/intellisense) for ARM templates will be active in VS Code as long as the file extension is **.json**.

From the blank `azuredeploy.json` file, type `arm!` and hit enter. As you type `arm!` you should see the following suggestion from IntelliSense.

```arm!   Skeleton ARM Template (User Snippet)```

This suggestion shows that on pressing enter, the skeleton of an ARM template file will be written to the empty file, containing the following:

```{
    "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "variables": {},
    "resources": [],
    "outputs": {}
}```

This shortcut pre-populates the required JSON structure of an ARM template file.

> Note that `armp!` is also an available suggestion; this shortcut pre-populates the required JSON structure for an ARM template parameter file. We will explore this ARM template parameter files later.


