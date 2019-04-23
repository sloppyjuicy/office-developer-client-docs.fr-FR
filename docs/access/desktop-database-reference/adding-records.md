---
title: Ajout d'enregistrements (référence de base de données de bureau Access)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280286"
---
# <a name="adding-records"></a>Ajout d’enregistrements

**S’applique à** : Access 2013, Office 2013

Utilisez la méthode **AddNew** pour créer et initialiser un nouvel enregistrement dans un objet **Recordset** existant. Vous pouvez utiliser la méthode **Supports** avec **CursorOptionEnum** affecté de la valeur **adAddNew** pour vérifier si vous pouvez ajouter des enregistrements à l'objet **Recordset** actif.

Après l'appel de la méthode **AddNew**, le nouvel enregistrement devient l'enregistrement actif et il le reste après l'appel de la méthode **Update**. Si l'objet **Recordset** ne prend pas en charge les signets, vous risquez de ne pas pouvoir accéder au nouvel enregistrement si vous passez à un autre. C'est pourquoi, en fonction du type de curseur, vous devrez peut-être appeler la méthode **Requery** pour rendre le nouvel enregistrement accessible.

Si vous appelez **AddNew** alors que vous modifiez l'enregistrement actif ou que vous en ajoutez un nouveau, ADO appelle la méthode **Update** pour enregistrer toute modification avant de créer le nouvel enregistrement.

Cette section contient les rubriques suivantes :

- [Ajout de plusieurs champs](adding-multiple-fields.md)
- [Détermination du mode d'édition](determining-edit-mode.md)
- [Utilisation de AddNew dans les modes immédiat et batch](using-addnew-in-immediate-and-batch-modes.md)

