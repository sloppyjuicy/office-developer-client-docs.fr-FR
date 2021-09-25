---
title: RaiseError, action de macro
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7bfeae06c337dd8770e0d724e1b53f3be6ccf0cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615199"
---
# <a name="raiseerror-macro-action"></a>RaiseError, action de macro

**S’applique à** : Access 2013, Office 2013 

L'action **DéclencherErreur** lève une exception qui peut être gérée par l'action de macro **[SurErreur](onerror-macro-action.md)**.

> [!NOTE]
> [!REMARQUE] L'action **DéclencherErreur** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètre

L’action **DéclencherErreur** utilise les arguments suivants.

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
<td><p>Numéro d’erreur</p></td>
<td><p>Oui</p></td>
<td><p>Nombre ou expression résolu au type de données Long.</p></td>
</tr>
<tr class="even">
<td><p>Description de l’erreur</p></td>
<td><p>Non</p></td>
<td><p>Expression de type Chaîne qui décrit l’erreur.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si l'action **DéclencherErreur** est appelée dans un événement de macro **[Avant la modification](before-change-macro-event.md)** ou **[Avant la suppression](before-delete-macro-event.md)**, l'événement est annulé.

S'il n'y a aucune instruction **SurErreur** active qui gère les erreurs, l'erreur levée par l'action **DéclencherErreur** est ajoutée à la table système **USysApplicationLog**. Lorsque l'action **DéclencherErreur** écrit dans la table **USysApplicationLog**, la colonne **Catégorie** prend automatiquement la valeur **Exécution**.

Pour afficher la table **USysApplicationLog**, procédez comme suit :

1.  Cliquez sur **le** menu Fichier, puis sur **Options.**

2.  Dans la boîte dialogue **Options Access**, cliquez sur l'onglet **Base de données active**.

3.  Dans la section **Navigation**, cliquez sur **Options de navigation**.

4.  Dans la boîte de dialogue **Options de navigation**, cliquez sur **Afficher les objets système**, puis sur **OK**.

5.  Cliquez sur **OK** pour fermer la boîte de dialogue **Options Access**.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action RaiseError pour annuler l’événement de macro de données Avant la modification. Lorsque le champ AssignedTo est mis à jour, un bloc de données LookupRecord est utilisé pour déterminer si le technicien affecté est actuellement affecté à une demande de service ouverte. Si c’est le cas, l’événement Before Change est annulé et l’enregistrement n’est pas mis à jour.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
