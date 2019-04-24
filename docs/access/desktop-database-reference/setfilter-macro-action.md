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
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308693"
---
# <a name="setfilter-macro-action"></a>SetFilter, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **AppliquerFiltre** pour appliquer un filtre aux enregistrements de la feuille de données, de l’état, de la table ou du formulaire actif.

## <a name="setting"></a>Setting

L’action **AppliquerFiltre** utilise les arguments suivants.

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
<td><p>Si spécifié, il s’agit du nom d’une requête ou d’un filtre enregistré en tant que requête. Cet argument ou l’argument Condition Where est obligatoire dans une base de données cliente. Dans une base de données Web, cet argument n'est pas disponible.</p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>S'il est fourni, une clause WHERE SQL qui limite les enregistrements d'une feuille de données, d'un formulaire, d'un état ou d'une table. Dans une base de données Web, cet argument est obligatoire.</p></td>
</tr>
<tr class="odd">
<td><p>Nom du contrôle</p></td>
<td><p>Si spécifié, il s'agit du nom du contrôle qui correspond au sous-formulaire ou sous-état à filtrer. Si cet argument est vide, l'objet actif est filtré.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Dans une base de données Web, l’argument Condition Where ne peut pas commencer par un signe égal (=).

Lorsque vous exécutez cette action, le filtre est appliqué à la table, au formulaire, à l'état ou à la feuille de données (par exemple les résultats de requête) qui est actif et qui a le focus.

La propriété **Filtre** de l'objet actif est utilisée pour enregistrer l'argument Condition Where et l'appliquer ultérieurement. Les filtres sont enregistrés avec les objets dans lesquels ils sont créés. Ils sont chargés automatiquement lors de l'ouverture de l'objet, mais ils ne sont pas appliqués automatiquement.

Dans une base de données cliente, pour appliquer automatiquement un filtre lors de l'ouverture de l'objet, affectez la valeur True à la propriété **FiltrerSurchargement**.

Dans une base de données Web, pour appliquer automatiquement un filtre lors de l’ouverture de l’objet, ajoutez l’action **AppliquerFiltre** à une macro et ajoutez la macro à l’événement **SurChargement** de l’objet.

## <a name="example"></a>Exemple

L'exemple suivant montre comment utiliser l'action SetFilter pour filtrer le formulaire dans lequel la macro est définie.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
