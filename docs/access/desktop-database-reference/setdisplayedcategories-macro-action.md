---
title: SetDisplayedCategories, action de macro
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711419"
---
# <a name="setdisplayedcategories-macro-action"></a>SetDisplayedCategories, action de macro


**S’applique à**: Access 2013, Office 2013

L'action **DéfinirCatégoriesAffichées** permet de spécifier les catégories affichées sous **Atteindre la catégorie** dans la barre de titre du volet de navigation. Par exemple, si vous souhaitez empêcher les utilisateurs de modifier le volet de navigation de façon à afficher les objets triés par **Date de création**, utilisez cette action pour masquer cette option dans la liste déroulante de la barre de titre.

## <a name="setting"></a>Valeur

L'action **DéfinirCatégoriesAffichées** accepte les arguments suivants.

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
<td><p><strong>Show</strong></p></td>
<td><p>Sélectionnez <strong>Oui</strong> pour afficher les catégories. Sélectionnez <strong>Non</strong> pour les masquer.</p></td>
</tr>
<tr class="even">
<td><p><strong>Catégorie</strong></p></td>
<td><p>Entrez ou sélectionnez le nom de la catégorie que vous souhaitez afficher ou masquer. Laissez ce champ vide pour afficher ou masquer toutes les catégories.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

  - La légende dans la barre de titre du volet de navigation indique le filtre activé, le cas échéant. Cliquez n'importe où dans la barre pour afficher la liste déroulante. Les éléments contrôlés par cette macro sont répertoriés sous **Atteindre la catégorie**.

  - Cette action active ou désactive uniquement l'affichage de la ou des catégories spécifiées ; elle ne modifie pas l'affichage du volet de navigation. Par exemple, si vous affichez les objets triés par **Date de création** et que vous utilisez l'action **DéfinirCatégoriesAffichées** pour désactiver l'option **Date de création**, Access n'affiche aucune autre catégorie dans le volet de navigation.

  - Pour exécuter l'action **DéfinirCatégoriesAffichées** dans un module VBA, utilisez la méthode **SetDisplayedCategories** de l'objet **DoCmd**.

