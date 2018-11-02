---
title: SetFilter, action de macro
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1b21c918f4a55d66cd4e7c7b91cd5612b6309619
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925564"
---
# <a name="setfilter-macro-action"></a>SetFilter, action de macro

**S’applique à**: Access 2013, Office 2013

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
<td><p>S'il est fourni, le nom d'une requête ou d'un filtre enregistré en tant que requête. Cet argument ou l’argument WhereCondition est nécessaire dans une base de données client. Dans une base de données web, cet argument n’est pas disponible.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>S'il est fourni, une clause WHERE SQL qui limite les enregistrements d'une feuille de données, d'un formulaire, d'un état ou d'une table. Dans une base de données web, cet argument est obligatoire.</p></td>
</tr>
<tr class="odd">
<td><p>Nom du contrôle :</p></td>
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
