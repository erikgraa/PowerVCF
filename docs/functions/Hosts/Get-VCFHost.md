# Get-VCFHost

### Synopsis
Connects to the specified SDDC Manager and retrieves a list of hosts.

### Description
The Get-VCFHost cmdlet connects to the specified SDDC Manager and retrieves a list of hosts.  
VCF Hosts are defined by a status
	- ASSIGNED - Hosts that are assigned to a Workload domain
	- UNASSIGNED_USEABLE - Hosts that are available to be assigned to a Workload Domain
	- UNASSIGNED_UNUSEABLE - Hosts that are currently not assigned to any domain and can be used for other domain tasks after completion of cleanup operation

### Examples
#### Example 1
```
Get-VCFHost
```
This example shows how to get all hosts regardless of status

#### Example 2
```
Get-VCFHost -Status ASSIGNED
```
This example shows how to get all hosts with a specific status

#### Example 3
```
Get-VCFHost -id edc4f372-aab5-4906-b6d8-9b96d3113304
```
This example shows how to get a host by id

#### Example 4
```
Get-VCFHost -fqdn sfo01-m01-esx01.sfo.rainpole.io
```
This example shows how to get a host by fqdn

### Parameters

#### -Status
- VCF Hosts are defined by status
	- ASSIGNED - Hosts that are assigned to a Workload domain
	- UNASSIGNED_USEABLE - Hosts that are available to be assigned to a Workload Domain
	- UNASSIGNED_UNUSEABLE - Hosts that are currently not assigned to any domain and can be used for other domain tasks after completion of cleanup operation

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

#### -id
ID of a specific host

```yaml
Type: String
Parameter Sets: Username
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

#### -fqdn
FQDN of a specific host

```yaml
Type: SecureString
Parameter Sets: Password
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Notes

### Related Links
