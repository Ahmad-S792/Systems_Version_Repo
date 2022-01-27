# Systems_Version_Details

It is tracker maintained to obtain script or others, using which we can find version details for each specific technology.

*Use Cases - ITGC Audits, IT Audits, Blue or Red Teaming

---

Following systems are tracked here:

## Operating Systems (OS)

- IBM AIX
- Sun Solaris / Oracle Solaris
- Red Hat Enterprise Linux (RHEL)
- Oracle Enterprise Linux (OEL)
- SuSE Enterprise Linux (SESL)
- Windows Server

## Databases (DB)

- Oracle Database (Oracle DB)
- Microsoft SQL Server (MSSQL)
- SAP HANA
- Sybase ASE
- UDB DB2 (IBM DB2 for all except z/OS)

## Enterprise Resource Planning (ERP)

- SAP ECC
- Oracle EBS
- BaaN ERP
- Microsoft Dynamics NAV
- Microsoft Dynamics AX

## Other Solutions

- Oracle Retail Management System (RMS)

## Hypervisor

- VMWare ESXi

---

| Systems                  	| Type       	| Execute In                  	| Method - 1                                        	| Method - 2                                                 	|
|--------------------------	|------------	|-----------------------------	|---------------------------------------------------	|------------------------------------------------------------	|
| Sun Solaris <10          	| OS         	| Terminal                    	| ```uname -a```                                    	| ```cat /etc/release```                                           	|
| Windows Server           	| OS         	| Command Prompt (CMD)        	| ```winver```                                            	| ```systeminfo \| findstr /B /C:"OS Name" /C:"OS Version"``` 	|
| SAP ECC                  	| ERP        	| SAP GUI                     	| Navigate to "SYSTEM" menu and select "STATUS"     	|                                                            	|
| Oracle EBS               	| ERP        	| SQL*Plus or other IDE       	| ```SELECT RELEASE_NAME FROM APPS.FND_PRODUCT_GROUPS;``` 	|                                                            	|
| Oracle Database          	| DB         	| SQL*Plus or other IDE       	| ```SELECT * FROM V$VERSION;```                           	| ```SELECT version FROM V$INSTANCE;```                            	|
| Microsoft SQL Server     	| DB         	| SQL Studio Management       	| ```SELECT @@VERSION```                     	|                                                            	|
| Red Hat Enterprise Linux 	| OS         	| Terminal                    	| ```cat /etc/redhat-release```                           	| ```hostnamectl```                                                         	|
| Oracle Enterprise Linux  	| OS         	| Terminal                    	| ```cat /etc/enterprise-release```                     	| ```/etc/oracle-release```                                        	|
| IBM AIX                  	| OS         	| Terminal                    	| ```oslevel -s```                                         	| ```oslevel -sq```                                                	|
| SAP Business One         	| ERP        	| SQL Studio Management       	| ```SELECT * FROM CINF;```                                	| ```SELECT * FROM SINF;```                                        	|
| SAP HANA                 	| DB         	| HDBSQL or HANA Studio       	| ```SELECT * FROM "SYS"."M_DATABASE";```                  	|                                                            	|
| BaaN ERP                 	| ERP        	| Session - Version Scan Tool 	| ```ttaad0500m000```                                     	|                                                            	|
| Sybase ASE               	| DB         	| ASE iSQL                    	| ```SELECT @@VERSION;```                               	|                                                            	|
| Oracle RMS               	| RMS        	| SQLPlus or other IDE       	| ```SELECT * FROM SYSTEM_OPTIONS;```                     	|                                                            	|
| SuSE Enterprise Linux    	| OS         	| Terminal                    	| ```cat /etc/os-release```                                	| ``` cat /etc/SuSE-release```                                       	|
| VMWare ESX               	| Hypervisor 	| Terminal                    	| ```vmware -v```                                      	|                                                            	|
| Microsoft Dynamics NAV   	| ERP        	| SQL Studio Management       	| ```SELECT [databaseversionno] FROM [$ndo$dbproperty]```  	|                                                            	|
| IBM zOS | Mainframe | Console | ```D IPLINFO``` | Go to Menu ISPF and navigate to option “7.3” and search for a variable “ZOS390RL” and issue the following command - “TSO ISPVCALL STATUS” |
