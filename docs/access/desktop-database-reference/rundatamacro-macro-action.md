---
title: ExécuterMacroDonnées, action de macro
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9790faf03ba0f6ea02520abb525c4301ac2181e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469557"
---
# <a name="rundatamacro-macro-action"></a>ExécuterMacroDonnées, action de macro

**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l'action **ExécuterMacroDonnées** pour exécuter une macro de données nommée.

## <a name="setting"></a>Paramètre

L'action **ExécuterMacroDonnées** utilise l'argument suivant.

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
<td><p>Name</p></td>
<td><p>Nom de la macro de données à exécuter.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Vous pouvez utiliser l'action **ExécuterMacroDonnées** dans des macros, des macros de données nommées et les événements de macros suivants : **[Événement de macro Après suppression](after-delete-macro-event.md)**, **[Événement de macro Après insertion](after-insert-macro-event.md)** et **[Événement de macro Après MAJ](after-update-macro-event.md)**.

Le nom de la macro de données doit inclure la table à laquelle elle est attachée (par exemple **Comments.AddComment**, pas seulement **AddComment**).

Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres. Si la macro de données nécessite des paramètres, les zones de texte apparaissent dans laquelle vous pouvez taper dans les arguments.

Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.

## <a name="example"></a>Exemple

L’exemple suivant montre comment passer un paramètre à une macro de données nommée. La macro de données dmGetCurrentServiceRequest de la table tblServiceRequests est appelée à l’aide de l’action ExécuterMacroDonnées. Lorsque la dmGetCurrentServiceRequest est terminée, la variable CurrentServiceRequest renvoyé formulaire que la macro de données est écrit dans la zone de texte txtCurrentSR.

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
