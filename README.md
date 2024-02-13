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

## Step1. Azure CLI Info Gathering (Only for Azure Database for PostgreSQL Single Servers)
1. Download the package zip file named `PostgreSQL-Info-Gather.zip`
2. Extract the `unzip PostgreSQL-Info-Gather.zip` file.
3. Run `rename rename.txt rename.bat` and Execute the `rename.bat` ( Windows ) 
4. Run `sh ./rename-linux.txt` ( Linux )
5. Open the Input file `Azure_Subscription.csv` and provide the Tenant ID & Subscription ID 
6. Execute `powershell.exe .\CMF-PostgreSQL-CLI-Windows.ps1` (Windows)
7. Execute `pwsh ./CMF-PostgreSQL-CLI-Linux.ps1` (Linux)
8. Once the execution completed, you can check the output & Logs folder.

## Step2. Update CMF_PostgreSQL_Server_Input_file.csv (For All Servers)
 "**Host_Name**","Resource_Group","**Port**","VCore","Auth_Type","**User_ID**","**Password**","**DB_Name**","Tenant","Subscription_ID","**Approval_Status**","**SSL_Mode**"

**Note:-**<br />
. Highlighted are **Mandatory Fields**<br />
. Update Mandatory fields manually in case of Azure VM / On-premises / Other Cloud Servers <br />

## Step3. PostgreSQL Server Info Gathering (For All Servers)
1. Execute `powershell.exe .\CMF-PostgreSQL-Windows.ps1` ( Windows )
2. Execute `pwsh ./CMF-PostgreSQL-Linux.ps1` ( Linux )
3. Once the execution completed, you can check the output & Logs folder.

## Step4. Azure VM/On-premises Servers  (Only for On-Premises / Azure VM / Other Cloud Servers)
. Refer document `CMF-ON-Prem_Server_Info_gather.docx` from the zip folder and update details and share document.<br />

Host-Name  | Cores | Memory | Storage Size | Storage Type | OS type | OS version | IOPS 

## Step5. Zip and share output, log folders (For All Servers) 
Kindly follow the execution instructions mentioned in attached documents. 
If there is/are any queries, please let us know, we will connect and check.

**Disclaimer:**
These scripts are intended for use of Info Gather Assessment utility and do not interact with the user databases or gather any sensitive information (e.g passwords, PI data etc.). 
These scripts are provided as-is to merely capture metadata information ONLY. While every effort has been made to ensure that accuracy and reliability of the scripts, 
it is recommended to review and test them in a non-production environment before deploying them in a production environment.
It is important to note that these scripts should be modified with consultation of Microsoft.
