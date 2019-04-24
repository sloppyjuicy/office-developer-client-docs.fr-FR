---
title: RunDataMacro, action de macro
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306810"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **ExécuterMacroDonnées** pour exécuter une macro de données nommée.

## <a name="setting"></a>Setting

L’action **ExécuterMacroDonnées** utilise l’argument suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nom</p></td>
<td><p>Nom de la macro de données à exécuter.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'action **RunDataMacro** dans les macros, les macros de données nommées et les événements de macros suivants: **[après suppression](after-delete-macro-event.md)** de l'événement de macro, après l'événement macro **[Insérer](after-insert-macro-event.md)** un événement de macro et **[après Maj](after-update-macro-event.md)**.

Le nom de la macro de données doit inclure le tableau auquel elle est attachée (par exemple, **comments.** AddComment, pas simplement AddComment). ****

Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres. Si la macro de données nécessite des paramètres, des zones de texte s'affichent à l'endroit où vous pouvez taper les arguments.

Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.

## <a name="example"></a>Exemple

L'exemple suivant montre comment transmettre un paramètre à une macro de données nommée. La macro de données dmGetCurrentServiceRequest de la table tblServiceRequests est appelée à l'aide de l'action RunDataMacro. Lorsque l'dmGetCurrentServiceRequest est terminé, la variable CurrentServiceRequest renvoyée est écrite dans la zone de texte txtCurrentSR.

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
