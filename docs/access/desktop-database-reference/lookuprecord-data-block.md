---
title: RechercherEnregistrement, bloc de données
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd9a687d7f74b99dc20ee079f970c37ba627f31
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877687"
---
# <a name="lookuprecord-data-block"></a>RechercherEnregistrement, bloc de données

**S’applique à**: Access 2013, Office 2013

Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.

> [!NOTE]
> [!REMARQUE] Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètre

L'action **DéfinirChamp** utilise les arguments suivants.

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
<td><p>Une chaîne qui identifie l’enregistrement à utiliser. L’argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</p>

> [!NOTE]
> L’enregistrement spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.


<p></p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>Non</p></td>
<td><p>Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données <strong>RechercherEnregistrement</strong> est effectuée. Par exemple, les critères sont souvent équivalents à la clause WHERE d’une expression SQL sans le mot où. Si les critères sont tous deux omis, le bloc de données <strong>RechercherEnregistrement</strong> opère sur l’intégralité du domaine spécifié par l’argument <em>dans</em> . Un champ qui est inclus dans les critères doit également être un champ <em>dans</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument <em>dans</em> . Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus. Si <em>Alias</em> n’est pas spécifié, le nom de la table ou de la requête est utilisé comme alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si les critères spécifiés par les arguments *dans* et *Condition Where* spécifie plusieurs enregistrements, le bloc de données **RechercherEnregistrement** fonctionne uniquement sur le premier enregistrement.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur d’une macro de données nommée. Un ReturnVar nommé **CurrentServiceRequest** est renvoyé à la macro ou de Visual Basic pour sous-routine Applications (VBA) qui a appelé la macro de données nommée.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

L’exemple suivant montre comment utiliser l’action Déclenchererreur pour annuler l’événement de macro de données avant la modification. Lorsque le champ AssignedTo est mis à jour, un bloc de données RechercherEnregistrement permet de déterminer si le technicien affecté est actuellement affecté à une demande de service en cours. Si la valeur est true, l’événement avant la modification est annulée et l’enregistrement n’est pas mis à jour.

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
