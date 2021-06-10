---
title: AddMenu, action de macro
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280272"
---
# <a name="addmenu-macro-action"></a>AddMenu, action de macro


**S’applique à** : Access 2013, Office 2013

Cet article décrit le fonctionnement de base de l’action de macro **AjouterMenu**.

Vous pouvez utiliser l’action **AjouterMenu** pour créer les éléments suivants :

- des menus personnalisés sous l'onglet **Compléments** d'un formulaire ou d'un état particulier ;

- un menu contextuel personnalisé pour un formulaire, un état ou un contrôle. Le menu contextuel personnalisé remplace le menu contextuel intégré pour le formulaire, l'état ou le contrôle ;

- un menu contextuel global. Le menu contextuel global remplace le menu contextuel intégré pour les champs des feuilles de données de table et de requête, des formulaires et des états, sauf là où vous avez ajouté un menu contextuel personnalisé pour un formulaire, un état ou un contrôle.

## <a name="setting"></a>Paramètre

L’action **AjouterMenu** possède les arguments suivants.

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
<td><p><strong>Nom du menu</strong></p></td>
<td><p>Nom du menu, par exemple, Commandes de rapport &quot; &quot; ou &quot; &quot; Outils. Pour créer une touche d’accès rapide qui vous permet de choisir le menu à l’aide du clavier, tapez une eterr e ( ) avant la lettre que vous souhaitez utiliser comme touche <strong>&amp;</strong> d’accès rapide. Cette lettre sera soulignée dans le nom de menu sous l’onglet <strong>Compléments</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de la macro de menu</strong></p></td>
<td><p>Nom du groupe de macros qui contient les macros pour les commandes du menu. Cet argument est obligatoire. 

</p>
<p><strong>REMARQUE</strong>: si vous exécutez une macro contenant l’action <strong>AjouterMenu</strong> dans une base de données bibliothèque, Microsoft Office Access 2007 recherche uniquement le groupe de macros de ce nom dans la base de données actuelle.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Texte de la barre d’état</strong></p></td>
<td><p>Texte à afficher dans la barre d’état lorsque le menu est sélectionné. Cet argument est ignoré pour les menus contextuels</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Pour exécuter l'action **AjouterMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **AddMenu** de l'objet **DoCmd**. Vous pouvez également définir la propriété **MenuBar** ou **ShortcutMenuBar** dans VBA pour créer un menu contextuel sous l'onglet **Compléments** ou pour attacher un menu contextuel personnalisé à un formulaire, un rapport ou un contrôle. Vous pouvez définir la propriété **ShortcutMenuBar** de l'objet **Application** pour créer un menu contextuel global.

