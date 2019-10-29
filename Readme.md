# CCS317252-Navigating Fabrication BIM Content With PowerBI

This is a deployable folder to use on your local Autodesk Imperial Fabrication Database (v3.06) with Power Bi

## Getting Started

- **For New Users:**
  - Run PBIDesktopSetup_x64.exe and PowerBIGatewayInstaller.exe to install PowerBi Desktop and the Gateway
    - [Power BI Desktop Download Link](https://www.microsoft.com/en-us/download/details.aspx?id=58494)
    - [Gateway Installer Link](https://powerbi.microsoft.com/en-us/gateway/)
  - _(If you already have PowerBi Desktop and the Gateway installed, skip to Setup)_

## Setup

1. Download and unpack this folder to your "C:\Users\ {YourUsernameHere} \Downloads\" directory.
2. Open the _v3UpdatedWHarrison.pbix_ file and click "Edit Queries" in the ribbon to open the Power Query Editor.
3. Open and Edit the Query Template files with your user account info and unpack location in the "Source=" line

- **Example If Unpacking to Desktop**

  - From:

    ```sql
    let
    Source = Excel.Workbook(File.Contents("C:\Users\{YourUsernameHere}\Downloads\CCS317252_AddlClassMaterials\ASTI_HarrisonImport.xlsx"), null, true),
    ```

  - To:

    ```sql
    let
    Source = Excel.Workbook(File.Contents("C:\Users\jsmith\Desktop\CCS317252_AddlClassMaterials\ASTI_HarrisonImport.xlsx"), null, true),
    ```

4. Paste modified scripts in the advanced editor window of each query

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
