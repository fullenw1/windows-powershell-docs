---
external help file: WssCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
title: New-WssStorageSpace
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-12-05
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: 949E85A4-124F-4AB5-B281-FD816987EACC
---

# New-WssStorageSpace

## SYNOPSIS
Creates a two-way mirrored storage space.

## SYNTAX

```
New-WssStorageSpace [-Force]
 [-Disk] <System.Collections.Generic.ICollection`1[Microsoft.WindowsServerSolutions.Storage.Disk]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-WssStorageSpace** cmdlet creates a two-way mirrored storage space on physical disks that you specify.

## EXAMPLES

### Example 1: Create a storage space
```
PS C:\> $Disks = Get-WssPoolableDisk
PS C:\> New-WssStorageSpace -Disk $Disks
```

The first command uses the Get-WssPoolableDisk cmdlet to get the available poolable disks, and stores them in the **$Disks** variable.

The second command creates a two-way mirrored storage space on the collection of disks stored in the **$Disks** variable.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disk
Specifies a collection of **Disk** objects.
The cmdlet creates a storage space on the disks that you specify.
To obtain **Disk** objects, use the Get-WssPoolableDisk cmdlet.

```yaml
Type: System.Collections.Generic.ICollection`1[Microsoft.WindowsServerSolutions.Storage.Disk]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.WindowsServerSolutions.Storage.Drive

## NOTES

## RELATED LINKS

[Get-WssPoolableDisk](./Get-WssPoolableDisk.md)

[Get-WssDisk](./Get-WssDisk.md)

[Add-WssDisksToSpacesPool](./Add-WssDisksToSpacesPool.md)

