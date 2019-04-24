---
title: WorkflowTasks, action de macro
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306005"
---
# <a name="workflowtasks-macro-action"></a>WorkflowTasks, action de macro


**S’applique à** : Access 2013, Office 2013

L’action **TâchesFluxTravail** permet d’afficher la boîte de dialogue **Tâche du flux de travail**.

## <a name="setting"></a>Setting

L’action **TâchesFluxTravail** utilise l’argument suivant :

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
<td><p><strong>Numéro d’enregistrement</strong></p></td>
<td><p>Position de l'élément dans la liste Microsoft SharePoint Foundation, à partir de <strong>1</strong> pour le premier élément de la liste, <strong>2</strong> pour le deuxième élément, et ainsi de suite. Vous pouvez également entrer une expression pour cet argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

  - L'action **TâchesFluxTravail** ouvre la boîte de dialogue **Tâches de flux de travail** qui affiche toutes les tâches disponibles pour l'élément spécifié. Un flux de travail doit être défini pour la liste dans SharePoint Foundation.

  - L'action **TâchesFluxTravail** ne peut être utilisée qu'après l'ouverture et la sélection d'une liste SharePoint Foundation liée. Pour ouvrir et sélectionner la liste liée, utilisez l'action **OuvrirTable**. Si la liste est déjà ouverte, utilisez l'action **SélectionnerObjet** pour la sélectionner.

  - Utiliser l'action **TâchesFluxTravail** équivaut à cliquer avec le bouton droit sur une cellule d'une liste SharePoint Foundation , ouverte en mode Feuille de données, à pointer sur **Flux de travail**, puis à cliquer sur **Tâches de flux de travail**.

  - Pour exécuter l'action **TâchesFluxTravail** dans un module VBA, utilisez la méthode **WorkflowTasks** de l'objet **DoCmd**.

