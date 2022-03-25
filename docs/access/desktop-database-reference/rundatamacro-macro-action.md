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
ms.localizationpriority: medium
ms.openlocfilehash: 595f36373ccd106aa2202fc0cc9e4814df5b7791
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724166"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **ExécuterMacroDonnées** pour exécuter une macro de données nommée.

## <a name="setting"></a>Setting

L’action **ExécuterMacroDonnées** utilise l’argument suivant.

<table>
<colgroup>
<col />
<col />
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

Vous pouvez utiliser l’action **ExécuterMacroDonnées** dans les macros, les macros de données nommées et les événements de macro suivants : événement de **[macro](after-delete-macro-event.md)** après suppression, événement de **[macro](after-insert-macro-event.md)** Après insertion et événement de macro Après mise à **[jour](after-update-macro-event.md)**.

Le nom de la macro de données doit inclure la table à laquelle elle est attachée (par exemple, **Comments.AddComment**, et pas seulement **AddComment**).

Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres. Si la macro de données requiert des paramètres, les zones de texte s’affichent là où vous pouvez taper les arguments.

Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.

## <a name="example"></a>Exemple

L’exemple suivant montre comment passer un paramètre à une macro de données nommée. La macro de données dmGetCurrentServiceRequest de la table tblServiceRequests est appelée à l’aide de l’action ExécuterMacroDonnées. Lorsque l’examen dmGetCurrentServiceRequest est terminé, la variable CurrentServiceRequest retourne le formulaire dans la zone de texte txtCurrentSR.

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
