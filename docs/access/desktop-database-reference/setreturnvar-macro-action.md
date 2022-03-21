---
title: SetReturnVar, action de macro
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 668425735b258d5f378ab91c7c71db61b7783e10
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634736"
---
# <a name="setreturnvar-macro-action"></a>SetReturnVar, action de macro

**S’applique à** : Access 2013, Office 2013

**L’action SetReturnVar** crée une variable de retour et la définit sur une valeur spécifique.

> [!NOTE]
> **L’action SetReturnVar** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètres

**L’action SetReturnVar** possède les arguments suivants.

<table>
<colgroup>
<col />
<col />
<col />
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
<td><p>Nom</p></td>
<td><p>Oui</p></td>
<td><p>Chaîne qui spécifie le nom de la variable.</p></td>
</tr>
<tr class="even">
<td><p>Expression</p></td>
<td><p>Oui</p></td>
<td><p>Expression qui sera utilisée pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression du signe égal (=). Vous pouvez cliquer sur le bouton <strong>Générer</strong> pour utiliser le <strong>Générateur d’expression</strong> pour définir cet argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

**L’action SetReturnVar** est utilisée pour créer une variable **ReturnVar**, qui peut être utilisée par les macros qui appellent une macro de données à l’aide de l’action **ExécuterMacroDonnées**.

Une fois **qu’unevar** de retour est créée par l’action **SetReturnVar** , la macro appelant peut l’utiliser dans une expression. Par exemple, si vous avez créé une variable **ReturnVar** nommée **UpdateSuccess**, vous pouvez utiliser la variable à l’aide de la syntaxe suivante :

```vb
    =[ReturnVars]![UpdateSuccess]
```

**L’action SetReturnVar** ne peut être utilisée que dans les macros de données nommées. Elle n’est pas disponible dans les macros de données attachées à un événement de macro de données.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur à partir d’une macro de données nommée. Une valeur ReturnVar **nommée CurrentServiceRequest** est renvoyée à la macro ou à la sous-Visual Basic pour Applications (VBA) qui a appelé la macro de données nommée.

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
