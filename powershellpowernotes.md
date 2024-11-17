# Active Directory Domain Services

## Module Installation

**Active Directory Domain Services** (AD DS) and related services form the core of Windows Server–based networks.

Use the Active Directory module for Windows PowerShell to automate AD DS administration with Windows PowerShell or PowerShell. 

The AD DS db is searchable, stores info about the network environment, offers a mechanism to configure and set the security on environment objects, and these tasks can be accomplished in bulk.

To install the AD module, add the corresponding Remote Server Administration Tools (RSAT) package (available since 2018 in Windows 10) for your operating system.

The list of available RSAT tools, can be found by going to `Optional features` in Settings, & selecting `Add a feature`.

Then select the option `RSAT: Active Directory Domain Services and Lightweight Directory Services Tools`.

## User management

The Active Directory module for Windows PowerShell cmdlets (User or Account in the noun) are used to create, modify, and delete user accounts, either individually or in bulk.

Identify the available cmdlets by using Get-Help or Get-Command & searching User or Account with a wildcard.

### Cmdlets for User Acount management

|---Cmdlet-------------|---------Description---------------|---------Examples----------------------------------------------------------|
|                      |                                   |                                                                           |
| New-ADUser 	         | Creates a user account            | `New-ADUser "Ana Bowman" -Department IT` Note: no password set = disabled |
| Get-ADUser 	         | Retrieves a user account          | `Get-ADUser -Identity anabowman -Properties Department,EmailAddress`      |
|                      |                                   |     All users: `Get-ADUser -Filter * -Properties *`                       |
| Set-ADUser           | Modify user account               |
| Remove-ADUser 	     | Deletes a user account            |
| Set-ADAccountPassword| Resets password of a user account |
| Unlock-ADAccount 	   | Unlocks a locked user account that|
|                      | has been locked after exceeding   |
|                      | the permitted number of incorrect |
|                      | sign-in attempts                  |
| Enable-ADAccount 	   | Enables a user account            |
| Disable-ADAccount 	 | Disables a user account           |
|                      |                                   |

### Common parameters for New-ADUser

|---Parameter-------------|---------Description---------------------------------------------------------|
| AccountExpirationDate 	| Defines the expiration date for a user account                              |
| AccountPassword 	      | Defines the password for a user account                                     |
| ChangePasswordAtLogon 	| Requires a user account to change passwords at the next sign-in             |
| Department 	            | Defines the department for a user account                                   |
| DisplayName 	          | Defines the display name for a user account                                 |
| HomeDirectory 	        | Defines the location of the home directory for a user account               |
| HomeDrive 	            | Defines the drive letters that map to the home directory for a user account |
| GivenName 	            | Defines the first name of a user account                                    |
