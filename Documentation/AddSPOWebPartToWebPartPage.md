#Add-SPOWebPartToWebPartPage
Adds a webpart to a web part page in a specified zone
##Syntax
```powershell
Add-SPOWebPartToWebPartPage -Path <String> -ServerRelativePageUrl <String> -ZoneId <String> -ZoneIndex <Int32> [-Web <WebPipeBind>]
```


```powershell
Add-SPOWebPartToWebPartPage -Xml <String> -ServerRelativePageUrl <String> -ZoneId <String> -ZoneIndex <Int32> [-Web <WebPipeBind>]
```


##Parameters
Parameter|Type|Required|Description
---------|----|--------|-----------
|Path|String|True|A path to a webpart file on a the file system.|
|ServerRelativePageUrl|String|True|Server Relative Url of the page to add the webpart to.|
|Web|WebPipeBind|False|The web to apply the command to. Omit this parameter to use the current web.|
|Xml|String|True|A string containing the XML for the webpart.|
|ZoneId|String|True||
|ZoneIndex|Int32|True||
##Examples

###Example 1
```powershell
PS:> Add-SPOWebPartToWebPartPage -ServerRelativePageUrl "/sites/demo/sitepages/home.aspx" -Path "c:\myfiles\listview.webpart" -ZoneId "Header" -ZoneIndex 1 
```
This will add the webpart as defined by the XML in the listview.webpart file to the specified page in the specified zone and with the order index of 1

###Example 2
```powershell
PS:> Add-SPOWebPartToWebPartPage -ServerRelativePageUrl "/sites/demo/sitepages/home.aspx" -XML $webpart -ZoneId "Header" -ZoneIndex 1 
```
This will add the webpart as defined by the XML in the $webpart variable to the specified page in the specified zone and with the order index of 1
