---
title: StartNewWorkflow, action de macro
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3752d0455d51d17108475e767380d2b1f0c2ef5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589077"
---
# <a name="startnewworkflow-macro-action"></a>StartNewWorkflow, action de macro


**S’applique à** : Access 2013, Office 2013

L'action **DémarrerNouveauFluxTravail** permet de lancer un nouveau flux de travail pour un élément dans une liste Microsoft SharePoint Foundation liée.

## <a name="setting"></a>Paramètre

L’action **DémarrerNouveauFluxTravail** utilise les arguments suivants :

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
<td><p>Position de l’élément dans la liste SharePoint Foundation, en commençant par <strong>1</strong> pour le premier élément de la liste, <strong>2</strong> pour le deuxième élément, etc. Vous pouvez également entrer une expression pour cet argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

  - L'action **DémarrerNouveauFluxTravail** ouvre la boîte de dialogue **Démarrer un nouveau flux de travail**. Cette boîte de dialogue affiche tous les flux de travail disponibles pour l'élément spécifié. Un flux de travail doit être défini pour la liste dans SharePoint Foundation avant d'être exécuté via cette action.

  - L'action **DémarrerNouveauFluxTravail** ne peut être utilisée qu'après l'ouverture et la sélection d'une liste SharePoint liée. Pour ouvrir et sélectionner la liste liée, utilisez l'action **OuvrirTable**. Si la liste est déjà ouverte, utilisez l'action **SélectionnerObjet** pour la sélectionner.

  - Utiliser l'action **DémarrerNouveauFluxTravail** équivaut à cliquer avec le bouton droit sur une cellule d'une liste SharePoint liée, ouverte en mode Feuille de données, à pointer sur **Flux de travail**, puis à cliquer sur **Démarrer un nouveau flux de travail**.

  - Pour exécuter l'action **DémarrerNouveauFluxTravail** dans un module VBA, utilisez la méthode **StartNewWorkflow** de l'objet **DoCmd**.

