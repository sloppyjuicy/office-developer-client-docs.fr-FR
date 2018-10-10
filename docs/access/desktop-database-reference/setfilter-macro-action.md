---
title: AppliquerFiltre, action de macro
TOCTitle: SetFilter Macro Action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fad18c6e7a9ca185e15598b532bbc6de4e5b4f9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471887"
---
# <a name="setfilter-macro-action"></a>AppliquerFiltre, action de macro

**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l'action **AppliquerFiltre** pour appliquer un filtre aux enregistrements de la feuille de données, de l'état, de la table ou du formulaire actif.

## <a name="setting"></a>Paramètre

L'action **AppliquerFiltre** utilise les arguments suivants.

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
<td><p>Nom du filtre</p></td>
<td><p>S'il est fourni, le nom d'une requête ou d'un filtre enregistré en tant que requête. Cet argument ou l’argument WhereCondition est nécessaire dans une base de données client. Dans une base de données Web, cet argument n’est pas disponible.</p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>Si spécifié, il s’agit d’une clause SQL WHERE qui restreint les enregistrements dans la feuille de données, le formulaire, l’état ou la table. Dans une base de données Web, cet argument est obligatoire.</p></td>
</tr>
<tr class="odd">
<td><p>Nom du contrôle</p></td>
<td><p>Si spécifié, il s'agit du nom du contrôle qui correspond au sous-formulaire ou sous-état à filtrer. Si cet argument est vide, l'objet actif est filtré.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Dans une base de données Web, l'argument Condition Where ne peut pas commencer par un signe égal (=).

Lorsque vous exécutez cette action, le filtre est appliqué à la table, au formulaire, à l'état ou à la feuille de données (par exemple les résultats de requête) qui est actif et qui a le focus.

La propriété **Filtre** de l'objet actif est utilisée pour enregistrer l'argument Condition Where et l'appliquer ultérieurement. Les filtres sont enregistrés avec les objets dans lesquels ils sont créés. Ils sont chargés automatiquement lors de l'ouverture de l'objet, mais ils ne sont pas appliqués automatiquement.

Dans une base de données cliente, pour appliquer automatiquement un filtre lors de l'ouverture de l'objet, affectez la valeur True à la propriété **FiltrerSurchargement**.

Dans une base de données Web, pour appliquer automatiquement un filtre lors de l'ouverture de l'objet, ajoutez l'action **AppliquerFiltre** à une macro et ajoutez la macro à l'événement **SurChargement** de l'objet.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action AppliquerFiltre pour filtrer le formulaire dans lequel la macro est définie.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
