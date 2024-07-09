# Connect-CloudBuilder

## Synopsis

Requests an authentication token from a VMware Cloud Builder instance.

## Syntax

```powershell
Connect-CloudBuilder [-fqdn] <String> [[-username] <String>] [[-password] <String>] [[-credential] <PSCredential>] [-skipCertificateCheck] [<CommonParameters>]
```

## Description

The `Connect-CloudBuilder` cmdlet connects to the specified VMware Cloud Builder instance and stores the credentials in a base64 string.

???+ note

    It is required once per session before running all other cmdlets.

## Examples

### Example 1

```powershell
Connect-CloudBuilder -fqdn sfo-cb01.sfo.rainpole.io -username admin -password VMw@re1!
```

This example shows how to connect to the specified VMware Cloud Builder instance.

### Example 2

```powershell
$secureString = Read-Host -AsSecureString 'Password'
Connect-CloudBuilder -fqdn sfo-cb01.sfo.rainpole.io -username admin -password $secureString
```

This example shows how to connect to the specified VMware Cloud Builder instance.

### Example 3

```powershell
Connect-CloudBuilder -fqdn sfo-cb01.sfo.rainpole.io -username admin
```

This example shows how to connect to the specified VMware Cloud Builder instance.
The operator will be prompted for a password.

### Example 4

```powershell
$credential = Get-credential
Connect-CloudBuilder -fqdn sfo-cb01.sfo.rainpole.io -credential $credential
```

This example shows how to connect to the specified VMware Cloud Builder instance.

### Example 5

```powershell
Connect-CloudBuilder -fqdn sfo-cb01.sfo.rainpole.io
```

This example shows how to connect to the VMware Cloud Builder instance.
The operator will be prompted for a username and password.

## Parameters

### -fqdn

The fully qualified domain name of the VMware Cloud Builder instance.

```yaml
Type: String
Parameter Sets: PSCredentialSet, UserNameAndPasswordSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -username

The username to authenticate to the VMware Cloud Builder instance.

```yaml
Type: String
Parameter Sets: UserNameAndPasswordSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -password

The password to authenticate to the VMware Cloud Builder instance. 
This parameter takes either a string or a SecureString variable.
If not specified, a SecureString variable will be prompted for.

```yaml
Type: String
Parameter Sets: UserNameAndPasswordSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -credential

Specifies a user account to authenticate to the SDDC Manager instance.

```yaml
Type: PSCredential
Parameter Sets: PSCredentialSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -skipCertificateCheck

Switch to skip certificate check when connecting to the VMware Cloud Builder instance.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### Common Parameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).
