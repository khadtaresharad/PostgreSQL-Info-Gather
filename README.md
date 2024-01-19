# Pre-requisites:
1. Windows 10, Windows Server 2012, Windows Server 2012 R2 and above
2. RHEL v7 & above, Ubuntu v7 & above, MacOS 
3. Azure CLI - Windows - https://aka.ms/installazurecliwindows   
               Linux - https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux/

# Steps To-Do:

## Azure CLI
1. Download the package zip file named `PostgreSQL-Info-Gather.zip`
2. Extract the `unzip PostgreSQL-Info-Gather.zip` file.
3. Run `rename rename.txt rename.bat` and Execute the `rename.bat` ( Windows ) 
4. Run `sh ./rename-linux.txt` ( Linux )
5. Open the Input file `Azure_Subscription.csv` and provide the Tenant ID & Subscription ID 
6. Execute `powershell.exe .\CMF-PostgreSQL-CLI-Windows.ps1` (Windows)
7. Execute `pwsh ./CMF-PostgreSQL-CLI-Linux.ps1` (Linux)
8. Once the execution completed, you can check the output & Logs folder.

## Azure VM/On-premises
 Please refer to document “CMF-ON-Prem_Server_Info_gather.docx” from the zip folder and share the details.

## Update CMF_PostgreSQL_Server_Input_file.csv 
 "**Host_Name**","Resource_Group","**Port**","VCore","Auth_Type","**User_ID**","**Password**","**DB_Name**","Tenant","Subscription_ID","**Approval_Status**","**SSL_Mode**"
 
 Note:- **Mandatory Fields**

## Server Info Gathering:
1. Execute `powershell.exe .\CMF-PostgreSQL-Windows.ps1` ( Windows )
2. Execute `pwsh ./CMF-PostgreSQL-Linux.ps1` ( Linux )
3. Once the execution completed, you can check the output & Logs folder.

## Zip and share output & log folders 

Kindly follow the execution instructions mentioned in attached documents. 
If there is/are any queries, please let us know, we will connect and check.
