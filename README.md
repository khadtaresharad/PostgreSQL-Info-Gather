# Steps To-Do:

# Pre-requisites
Supported OS<br />
Windows 10, Windows Server 2012, Windows Server 2012 R2 and above
Linux RHEL v7 & above, Ubuntu v14 & above

Powershell (Install)<br /> 
Windows - https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4<br /> 
Linux   - https://learn.microsoft.com/en-us/powershell/scripting/install/install-rhel?view=powershell-7.4<br /> 

Azure CLI (Install Only for Azure workloads like single server assessments)<br /> 
Windows - https://aka.ms/installazurecliwindows <br />
Linux   - https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux/<br /> 

PostgreSQL Client (Install on supported OS ) <br />
Windows - https://www.postgresql.org/download/windows/ <br />
Linux - https://www.postgresql.org/download/linux/ <br />

 **Note**: - <br />
Add PATH in Enviornment Variables (Windows)<br />
`Azure CLI  ( e.g. C:\Program Files\Microsoft SDKs\Azure\CLI2\wbin )`<br />
`PostgreQL Client ( e.g. C:\Program Files\PostgreSQL\bin )<br />`

# Steps To-Do:

## Step1. Azure CLI Info Gathering ( Only for Azure Database for PostgreSQL Single Servers )
1. Download the package zip file named `PostgreSQL-Info-Gather.zip`
2. Extract the `unzip PostgreSQL-Info-Gather.zip` file.
3. Run `rename rename.txt rename.bat` and Execute the `rename.bat` ( Windows ) 
4. Run `sh ./rename-linux.txt` ( Linux )
5. Open the Input file `Azure_Subscription.csv` and provide the Tenant ID & Subscription ID 
6. Execute `powershell.exe .\CMF-PostgreSQL-CLI-Windows.ps1` (Windows)
7. Execute `pwsh ./CMF-PostgreSQL-CLI-Linux.ps1` (Linux)
8. Once the execution completed, you can check the output & Logs folder.

## Step2. Update CMF_PostgreSQL_Server_Input_file.csv (Mandatory)
 "**Host_Name**","Resource_Group","**Port**","VCore","Auth_Type","**User_ID**","**Password**","**DB_Name**","Tenant","Subscription_ID","**Approval_Status**","**SSL_Mode**"

**Note:-**<br />
. Highlighted are **Mandatory Fields**<br />
. Update Mandatory fields manually in case of Azure VM / On-premises / Other Cloud Servers <br />

## Step3. PostgreSQL Server Info Gathering (Mandatory)
1. Execute `powershell.exe .\CMF-PostgreSQL-Windows.ps1` ( Windows )
2. Execute `pwsh ./CMF-PostgreSQL-Linux.ps1` ( Linux )
3. Once the execution completed, you can check the output & Logs folder.

## Step4. Azure VM/On-premises Servers  ( Only for On-Premises / Azure VM / Other Cloud Servers )
. Refer document `CMF-ON-Prem_Server_Info_gather.docx` from the zip folder and update details and share document.<br />

Host-Name  | Cores | Memory | Storage Size | Storage Type | OS type | OS version | IOPS 

## Step5. Zip and share output, log folders (Mandatory) 
Kindly follow the execution instructions mentioned in attached documents. 
If there is/are any queries, please let us know, we will connect and check.

**Disclaimer:**
The following PowerShell scripts provided are intended for use as a Info Gather utility tool and do not directly interact with the user database server or store any sensitive information, including passwords. These scripts are provided as-is without any warranty, express or implied.
While every effort has been made to ensure the accuracy and reliability of the scripts, it is recommended to review and test them in a non-production environment before deploying them in a production environment.
It is important to note that these scripts should not be used to directly modify or interact with the database server without proper understanding and consideration of potential impacts on the server and data integrity.
Furthermore, these scripts do not handle sensitive information such as passwords directly within the script. It is the responsibility of the user to ensure that any sensitive information, including passwords, is handled securely and in compliance with organizational security policies.
By using these scripts, you acknowledge and agree that the authors and contributors shall not be liable for any damages or losses arising from the use of these scripts.
