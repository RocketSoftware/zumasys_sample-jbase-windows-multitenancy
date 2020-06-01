# jBASE Windows Multi Tenancy Example

This project demonstrates a Multi Tenancy setup.  This is a Windows project but it can be easily modified to work with Unix.

1. Change the .bat files to .sh files. 
2. Change the SET statements to export statements
3. Adjust the paths correctly
4. Within each SYSTEM file you must adjust all the paths.

## Usage

By default this projects expects to be in c:\dbms.  Once you unzip or clone this project change the root directory accordingly.

## Admin Account

```
c:
cd \dbms\global
admin.bat
LOGTO ADMIN
```

This is a generic admin account.  It has it's own system file that has information for the other tenants.  You can LOGTO each tenant.  It is NOT setup to adjust the LIST file and SPOOLER. 

## Tenant Account

```
c:
cd \dbms\tenants\tenant1
tenant1.bat
LOGTO TENANT1
```

Each tenant has it's own system file.  It can only see it's own system. 

1. Unique ports are assigne
2. Unique list file is assigned (CALLED POINTER-FILE IN THE MD).
3. Unique spooler.  You can restart it with SP-NEWTAB
4. You can create additional accounts within this tenant.


