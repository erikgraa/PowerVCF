# Set-VCFCredential

### Synopsis
Connects to the specified SDDC Manager and updates a credential.

### Syntax
```
Set-VCFCredential -json <path to json file>
```

### Description
The Set-VCFCredential cmdlet connects to the specified SDDC Manager and updates a credential.
Credentials can be updated with a specified password(s) or rotated using system generated password(s).

### Examples
#### Example 1
```
Set-VCFCredential -json .\Credential\updateCredentialSpec.json
```
This example shows how to update a credential using a json spec

### Parameters

#### -json
- Path to JSON file with credentials to be updated

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accepted Value: Resource FQDN
```
### Sample JSON
#### Update Credentials with specified password
```
{
  "operationType" : "UPDATE",
  "elements" : [ {
    "resourceName" : "sfo01-m01-esx02.sfo.rainpole.io",
    "resourceType" : "ESXI",
    "credentials" : [ {
      "credentialType" : "SSH",
      "username" : "root",
      "password" : "VMwareInfra@1"
    } ]
  } ]
}

```
#### Rotate Credentials with system defined password
```
{
  "operationType" : "ROTATE",
  "elements" : [ {
    "resourceName" : "sfo01-m01-esx02.sfo.rainpole.io",
    "resourceType" : "ESXI",
    "credentials" : [ {
      "credentialType" : "SSH",
      "username" : "root"
    } ]
  } ]
}

```

### Notes

### Related Links
Steps to configure Dual Authentication https://docs.vmware.com/en/VMware-Cloud-Foundation/3.9/com.vmware.vcf.ovdeploy.doc_39/GUID-FAB78718-E626-4924-85DC-97536C3DA337.html
