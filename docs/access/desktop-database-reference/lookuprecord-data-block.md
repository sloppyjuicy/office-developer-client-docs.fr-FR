---
title: Bloc de données LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734209"
---
# <a name="lookuprecord-data-block"></a>Bloc de données LookupRecord

**S’applique à** : Access 2013, Office 2013

Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.

> [!NOTE]
> Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Setting

L’action **DéfinirChamp** utilise les arguments suivants.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatoire</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Dans le paramètre</p></td>
<td><p>Oui</p></td>
<td><p>Chaîne qui identifie l’enregistrement sur lequel opérer. <em>L’argument In</em> peut contenir le nom de la table, une requête Select ou une SQL instruction.</p><p><strong>REMARQUE</strong>: l’enregistrement spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>Non</p></td>
<td><p>Expression de type Chaîne qui permet de restreindre la plage de données sur laquelle opère le bloc de données <strong>RechercherEnregistrement</strong>. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. Si des critères sont omis, le bloc de données <strong>LookupRecord</strong> fonctionne sur l’intégralité du domaine spécifié par l’argument <em>In.</em> Tout champ inclus dans les critères doit également être un champ dans <em>In</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument <em>In.</em> On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës. Si <em>Alias</em> n’est pas spécifié, le nom de la table ou de la requête est utilisé comme alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si les critères spécifiés par les arguments Condition *In* et *Where* renvoient plusieurs enregistrement, le bloc de données **LookupRecord** fonctionne uniquement sur le premier enregistrement.  Si aucun enregistrement ne correspond aux critères spécifiés, Access ignore l’ensemble des actions contenues dans le bloc **LookupRecord,** comme s’il s’agit d’une expression de bloc de macro **[If](if-then-else-macro-block.md)** évaluée comme false.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur à partir d’une macro de données nommée. Une valeur ReturnVar nommée **CurrentServiceRequest** est renvoyée à la macro ou à la sous-Visual Basic pour Applications (VBA) qui a appelé la macro de données nommée.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

L’exemple suivant montre comment utiliser l’action RaiseError pour annuler l’événement de macro de données Avant la modification. Lorsque le champ AssignedTo est mis à jour, un bloc de données LookupRecord est utilisé pour déterminer si le technicien affecté est actuellement affecté à une demande de service ouverte. Si c’est le cas, l’événement Before Change est annulé et l’enregistrement n’est pas mis à jour.

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
