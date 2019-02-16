# Lab 3 - First Template



## Create a template file

From **Visual Studio Code (VS Code)**, open a working directory such as `C:\Temp\armlabs`

Create a new folder such as `FirstTemplate`

Create a new file named `azuredeploy.json`. **azuredeploy.json** is the standard naming convention for an ARM template file, however any filename will work successfully. [IntelliSense](https://code.visualstudio.com/docs/editor/intellisense) for ARM templates will be active in VS Code as long as the file extension is **.json**.

From the blank `azuredeploy.json` file, type `arm!` and hit enter. As you type `arm!` you should see the following suggestion from IntelliSense.

```arm!   Skeleton ARM Template (User Snippet)```

This suggestion shows that on pressing enter, the skeleton of an ARM template file will be written to the empty file, containing the following:

```
{
    "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "variables": {},
    "resources": [],
    "outputs": {}
}
```

This shortcut pre-populates the required JSON structure of an ARM template file.

> Note that `armp!` is also an available suggestion; this shortcut pre-populates the required JSON structure for an ARM template parameter file. We will explore this ARM template parameter files later.

## Add a Virtual Network resource to the template

With in the square brackets following resources, press enter to create a new line:

```
"resources": [

],
```

On the new line type `arm-` to begin IntelliSense suggestions.

Note that using the hypen will show suggestions for many ARM resources from the snippets. We are looking to deploy a virtual network, so scroll through of complete the suggetion `arm-vn` and then press enter to complete the virtual network basic structure.

```
{
    "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "variables": {},
    "resources": [
        {
            "apiVersion": "2015-06-15",
            "type": "Microsoft.Network/virtualNetworks",
            "name": "VirtualNetwork1",
            "location": "[resourceGroup().location]",
            "tags": {
                "displayName": "VirtualNetwork1"
            },
            "properties": {
                "addressSpace": {
                    "addressPrefixes": [
                        "10.0.0.0/16"
                    ]
                },
                "subnets": [
                    {
                        "name": "Subnet-1",
                        "properties": {
                            "addressPrefix": "10.0.0.0/24"
                        }
                    },
                    {
                        "name": "Subnet-2",
                        "properties": {
                            "addressPrefix": "10.0.1.0/24"
                        }
                    }
                ]
            }
        }
    ],
    "outputs": {}
}
```

> Note: This is not complete information for a virtual network, to see the full reference for properties not defined here (such as Peering) visit the ARM template reference pages here: [aka.ms/armref](https://aka.ms/armref).
