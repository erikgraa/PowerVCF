# Request-VCFToken

## Synopsis

Requests an authentication token from SDDC Manager.

## Syntax

```powershell
Request-VCFToken [-Fqdn] <String> [[-UserName] <String>] [[-Password] <String>] [[-Credential] <PSCredential>] [-SkipCertificateCheck] [<CommonParameters>]
```

## Description

The `Request-VCFToken` cmdlet connects to the specified SDDC Manager and requests API access and refresh tokens. It is required once per session before running all other cmdlets.

## Examples

### Example 1

```powershell
Request-VCFToken -Fqdn sfo-vcf01.sfo.rainpole.io -UserName administrator@vsphere.local -Password VMw@re1!
```

This example shows how to connect to the specified SDDC Manager to request API access and refresh tokens.

### Example 2

```powershell
$secureString = Read-Host -AsSecureString 'Password'
Request-VCFToken -Fqdn sfo-vcf01.sfo.rainpole.io -UserName admin@local -Password $secureString
```

This example shows how to connect to the SDDC Manager instance using local account `admin@local`.

### Example 3

```powershell
Request-VCFToken -Fqdn sfo-vcf01.sfo.rainpole.io -UserName admin@local
```

This example shows how to connect to the SDDC Manager instance using local account `admin@local`.
The operator will be prompted for a password.

### Example 4

```powershell
$credential = Get-Credential
Request-VCFToken -Fqdn sfo-vcf01.sfo.rainpole.io -Credential $credential
```

This example shows how to connect to the SDDC Manager instance.

### Example 5

```powershell
Request-VCFToken -Fqdn sfo-vcf01.sfo.rainpole.io
```

This example shows how to connect to the SDDC Manager instance.
The operator will be prompted for a username and password.

## Parameters

### -Fqdn

The fully qualified domain name or IP Address of the SDDC Manager instance.

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

### -UserName

The username to authenticate to the SDDC Manager instance.

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

### -Password

The password to authenticate to the SDDC Manager instance. 
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

### -Credential

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

### -SkipCertificateCheck

Switch to skip certificate check when connecting to the SDDC Manager instance.

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