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
ms.localizationpriority: medium
ms.openlocfilehash: 97c5c3bd337785e4222655538310a194ee45e8cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593283"
---
# <a name="workflowtasks-macro-action"></a>WorkflowTasks, action de macro


**S’applique à** : Access 2013, Office 2013

L’action **TâchesFluxTravail** permet d’afficher la boîte de dialogue **Tâche du flux de travail**.

## <a name="setting"></a>Paramètre

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
<td><p>Position de l’élément dans la liste Microsoft SharePoint Foundation, en commençant par <strong>1</strong> pour le premier élément de la liste, <strong>2</strong> pour le deuxième élément, etc. Vous pouvez également entrer une expression pour cet argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

  - L'action **TâchesFluxTravail** ouvre la boîte de dialogue **Tâches de flux de travail** qui affiche toutes les tâches disponibles pour l'élément spécifié. Un flux de travail doit être défini pour la liste dans SharePoint Foundation.

  - L'action **TâchesFluxTravail** ne peut être utilisée qu'après l'ouverture et la sélection d'une liste SharePoint Foundation liée. Pour ouvrir et sélectionner la liste liée, utilisez l'action **OuvrirTable**. Si la liste est déjà ouverte, utilisez l'action **SélectionnerObjet** pour la sélectionner.

  - Utiliser l'action **TâchesFluxTravail** équivaut à cliquer avec le bouton droit sur une cellule d'une liste SharePoint Foundation , ouverte en mode Feuille de données, à pointer sur **Flux de travail**, puis à cliquer sur **Tâches de flux de travail**.

  - Pour exécuter l'action **TâchesFluxTravail** dans un module VBA, utilisez la méthode **WorkflowTasks** de l'objet **DoCmd**.

