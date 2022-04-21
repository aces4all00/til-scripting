There are 2 basic methods for using PowerShell to get information about a specific Active Directory user account (some user with SamAccountName 'someUser' in my examples):

```PowerShell
Get-ADUser -identity 'someUser'
```

Use of the `-identity` parameter assumes you are looking for a known object that should exist. If no such object exists a non terminating (by default) error is thrown. 

```PowerShell
Get-ADUser -filter {SamAccountName -eq 'someUser'}
```

Use of the `-filter` parameter to find where an identity (unique) field (DistinguishedName, ObjectGuid, ObjectSid, SamAccountName) is equal to the supplied value ***does not assume*** you are looking for a known object that should exist, only returning any such object that does exist. No error is thrown when no such object exists.