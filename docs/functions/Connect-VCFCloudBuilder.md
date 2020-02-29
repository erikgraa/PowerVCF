# Connect-VCFCloudBuilder

### Synopsis
Connects to the specified Cloud Builder appliance and stores the credentials in a base64 string

### Syntax
```
Connect-VCFCloudBuilder -fqdn <String> -Username <String> -Password <String>
```

### Description
The Connect-VCFCloudBuilder cmdlet connects to the specified Cloud Builder appliance and stores the
credentials in a base64 string. It is required once per session before running the SDDC cmdlets

### Examples
#### Example 1
```
Connect-VCFCloudBuilder -fqdn sfo01cb01.sfo.rainpole.local -username admin -password VMware1!
```
This example shows how to connect to Cloud Builder appliance

### Parameters

#### -fqdn
The fully qualified domain name of the Cloud Builder appliance to connect to

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

#### -Username
Username to connect with
Currently supported with admin account only

```yaml
Type: String
Parameter Sets: Username
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

#### -Password
Password to connect with

```yaml
Type: SecureString
Parameter Sets: Password
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Notes

### Related Links
