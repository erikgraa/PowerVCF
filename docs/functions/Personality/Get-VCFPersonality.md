# Get-VCFPersonality

### Synopsis
Get the vSphere Lifecycle Manager personalities

### Syntax
```
Get-VCFPersonality -id <string>
```

### Description
The Get-VCFPersonality cmdlet gets the vSphere Lifecycle Manager personalities which are available via depot access

### Examples
#### Example 1
```
Get-VCFPersonality
```
This example list all the vSphere Lifecycle Manager personalities availble in the depot

#### Example 2
```
Get-VCFPersonality -id b4e3b2c4-31e8-4816-b1c5-801e848bef09
```
This example gets a vSphere Lifecycle Manager personality by ID

### Parameters

#### -id
ID of the personality

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

### Notes

### Related Links
