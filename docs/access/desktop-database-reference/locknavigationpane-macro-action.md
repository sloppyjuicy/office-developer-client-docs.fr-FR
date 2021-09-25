---
title: LockNavigationPane, action de macro
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6682d42754fac7780241a069e5f043728ad883da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594005"
---
# <a name="locknavigationpane-macro-action"></a>LockNavigationPane, action de macro


**S’applique à** : Access 2013, Office 2013

Utilisez l'action **VerrouillerVoletNavigation** pour empêcher les utilisateurs de supprimer des objets de base de données qui sont affichés dans le volet de navigation.

## <a name="setting"></a>Paramètre

L’action **VerrouillerVoletNavigation** possède les arguments suivants.

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
<td><p><strong>Lock</strong></p></td>
<td><p>Sélectionnez <strong>Oui</strong> pour verrouiller le volet de navigation ou <strong>Non</strong> pour déverrouiller le volet de navigation.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Verrouiller le volet de navigation vous empêche de supprimer des objets de base de données ou de les couper pour les placer dans le Presse-papiers. En revanche, cette action ne vous empêche *pas* d’effectuer les opérations suivantes :

  - copier des objets de base de données dans le Presse-papiers ;

  - coller des objets de base de données à partir du Presse-papiers ;

  - afficher ou masquer le volet de navigation ;

  - sélectionner d'autres modèles d'organisation du volet de navigation ;

  - afficher ou masquer des sections du volet de navigation.

Pour exécuter l'action **VerrouillerVoletNavigation** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **LockNavigationPane** de l'objet **DoCmd**.

