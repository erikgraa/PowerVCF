# Get-VCFManager

### Synopsis
Get a list of SDDC Managers

### Syntax
```
Get-VCFManager -id <string>
```

### Description
The Get-VCFManager cmdlet retrieves the SDDC Manager details

### Examples
#### Example 1
```
Get-VCFManager
```
This example shows how to retrieve a list of SDDC Managers  

#### Example 2
```
Get-VCFManager -id 60d6b676-47ae-4286-b4fd-287a888fb2d0
```
This example shows how to return the details for a specific SDDC Manager based on the ID  

#### Example 3
```
Get-VCFManager -domainId 1a6291f2-ed54-4088-910f-ead57b9f9902
```
This example shows how to return the details for a specific SDDC Manager based on a domain ID  

### Parameters

#### -id
- ID of a specific SDDC Manager

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
```

#### -domainId
- ID of a specific domain

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
```

### Notes

### Related Links
