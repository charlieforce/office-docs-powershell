---
external help file: Microsoft.Exchange.WebClient-Help.xml
online version: https://docs.microsoft.com/powershell/module/exchange/new-publicfolderdatabase
applicable: Exchange Server 2010
title: New-PublicFolderDatabase
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
---

# New-PublicFolderDatabase

## SYNOPSIS
This cmdlet is available only in Exchange Server 2010.

Use the New-PublicFolderDatabase cmdlet to create a public folder database.

For information about the parameter sets in the Syntax section below, see [Exchange cmdlet syntax](https://docs.microsoft.com/powershell/exchange/exchange-cmdlet-syntax).

## SYNTAX

```
New-PublicFolderDatabase [-Name] <String> -Server <ServerIdParameter>
 [-Confirm]
 [-DomainController <Fqdn>]
 [-EdbFilePath <EdbFilePath>]
 [-LogFolderPath <NonRootLocalLongFullPath>]
 [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The new database must be mounted after it's created. For more information about mounting databases, see [Mount a Database](https://docs.microsoft.com/previous-versions/office/exchange-server-2010/bb123587(v=exchg.141)).

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see [Find the permissions required to run any Exchange cmdlet](https://docs.microsoft.com/powershell/exchange/find-exchange-cmdlet-permissions).

## EXAMPLES

### Example 1
```powershell
New-PublicFolderDatabase -Name "My Public Folder Database" -EdbFilePath "C:\Program Files\Microsoft\Exchange Server\V14\Mailbox\PFDB01.edb" -LogFolderPath "C:\Program Files\Microsoft\Exchange Server\V14\Mailbox\PFDB01"
```

This example creates the public folder database PFDB01.

## PARAMETERS

### -Name
The Name parameter specifies the name of the new public folder database. The name must be unique to your entire organization.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
The Server parameter specifies the Mailbox server where you want to create the new public folder database. You can use any value that uniquely identifies the server. For example:

- Name
- FQDN
- Distinguished name (DN)
- Exchange Legacy DN

A server can have only one public folder database.

```yaml
Type: ServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: `-Confirm:$false`.
- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EdbFilePath
The EdbFilePath parameter specifies the full path of the public folder database files. The default location is `%ExchangeInstallPath%Mailbox\<Public Folder DB Name>\<Public Folder DB Name>.edb`

```yaml
Type: EdbFilePath
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogFolderPath
The LogFolderPath parameter specifies the folder location for log files. The default location is `%ExchangeInstallPath%Mailbox\<Public Folder DB Name>`.

```yaml
Type: NonRootLocalLongFullPath
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### Input types
To see the input types that this cmdlet accepts, see [Cmdlet Input and Output Types](https://go.microsoft.com/fwlink/p/?LinkId=2081749). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

### Output types
To see the return types, which are also known as output types, that this cmdlet accepts, see [Cmdlet Input and Output Types](https://go.microsoft.com/fwlink/p/?LinkId=2081749). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS
