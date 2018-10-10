---
title: SetReturnVar Macro Action
TOCTitle: SetReturnVar Macro Action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa4380904888194bf1d954ebf5619cab7d155047
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470253"
---
# <a name="setreturnvar-macro-action"></a>SetReturnVar Macro Action

**S’applique à**: Access 2013 | Office 2013

L’action **SetReturnVar** crée une variable de renvoi et lui affecte une valeur spécifique.

> [!NOTE]
> L’action **SetReturnVar** est disponible uniquement dans les Macros de données.

## <a name="setting"></a>Paramètre

L’action **SetReturnVar** possède les arguments suivants.

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
<td><p>Name</p></td>
<td><p>Oui</p></td>
<td><p>Chaîne qui spécifie le nom de la variable.</p></td>
</tr>
<tr class="even">
<td><p>Expression</p></td>
<td><p>Oui</p></td>
<td><p>Une expression qui sera utilisée pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression avec le signe égal (=). Vous pouvez cliquer sur le bouton <strong>Générer</strong> pour utiliser le <strong>Générateur d’Expression</strong> pour définir cet argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’action **SetReturnVar** est utilisée pour créer un **ReturnVar**, qui est la variable peut être utilisé par des macros qui appeler une macro de données à l’aide de l’action **ExécuterMacroDonnées** .

Une fois qu’un **ReturnVar** est créé par l’action **SetReturnVar** , la macro appelante peut l’utiliser dans une expression. Par exemple, si vous avez créé un **ReturnVar** nommé **UpdateSuccess**, vous pouvez utiliser la variable à l’aide de la syntaxe suivante :

```vb
    =[ReturnVars]![UpdateSuccess]
```

L’action **SetReturnVar** peut être utilisée uniquement dans les macros de données nommée. Il n’est pas disponible dans les macros de données associées à un événement de macro de données.

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
