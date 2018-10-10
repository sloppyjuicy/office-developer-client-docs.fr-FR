---
title: VerrouillerVoletNavigation, action de macro
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4e18b17c5d00095b61323511c20b95a355819eab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471703"
---
# <a name="locknavigationpane-macro-action"></a>VerrouillerVoletNavigation, action de macro


**S’applique à**: Access 2013 | Office 2013

Utilisez l'action **VerrouillerVoletNavigation** pour empêcher les utilisateurs de supprimer des objets de base de données qui sont affichés dans le volet de navigation.

## <a name="setting"></a>Valeur

L'action **VerrouillerVoletNavigation** possède les arguments suivants.

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

Verrouiller le volet de navigation vous empêche de supprimer des objets de base de données ou de les couper pour les placer dans le Presse-papiers. Il fait *pas* vous empêcher d’effectuer l’une des opérations suivantes :

  - copier des objets de base de données dans le Presse-papiers ;

  - coller des objets de base de données à partir du Presse-papiers ;

  - afficher ou masquer le volet de navigation ;

  - sélectionner d'autres modèles d'organisation du volet de navigation ;

  - afficher ou masquer des sections du volet de navigation.

Pour exécuter l'action **VerrouillerVoletNavigation** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **LockNavigationPane** de l'objet **DoCmd**.

