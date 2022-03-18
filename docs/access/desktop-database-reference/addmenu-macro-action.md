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
ms.localizationpriority: medium
ms.openlocfilehash: 9e78bfc5ba999beaad1840b0a1dca9f1d2545be0
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558634"
---
# <a name="addmenu-macro-action"></a>AddMenu, action de macro


**S’applique à** : Access 2013, Office 2013

Cet article décrit le fonctionnement de base de l’action de macro **AjouterMenu**.

Vous pouvez utiliser l’action **AjouterMenu** pour créer les éléments suivants :

- des menus personnalisés sous l'onglet **Compléments** d'un formulaire ou d'un état particulier ;

- un menu contextuel personnalisé pour un formulaire, un état ou un contrôle. Le menu contextuel personnalisé remplace le menu contextuel intégré pour le formulaire, l'état ou le contrôle ;

- un menu contextuel global. Le menu contextuel global remplace le menu contextuel intégré pour les champs des feuilles de données de table et de requête, des formulaires et des états, sauf là où vous avez ajouté un menu contextuel personnalisé pour un formulaire, un état ou un contrôle.

## <a name="setting"></a>Paramètres

L’action **AjouterMenu** possède les arguments suivants.

<table>
<colgroup>
<col />
<col />
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
<td><p>Nom du menu, par exemple, &quot;Commandes de rapport ou &quot;Outils&quot;&quot;. Pour créer une touche d’accès rapide qui vous permet de choisir le menu à l’aide du clavier, tapez une eterr e (<strong>&amp;</strong>) avant la lettre que vous souhaitez utiliser comme touche d’accès rapide. Cette lettre sera soulignée dans le nom de menu sous l’onglet <strong>Compléments</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de la macro de menu</strong></p></td>
<td><p>Nom du groupe de macros qui contient les macros pour les commandes du menu. Cet argument est obligatoire. 

</p>
<p><strong>REMARQUE</strong> : si vous exécutez une macro contenant l’action <strong>AjouterMenu</strong> dans une base de données bibliothèque, Microsoft Office Access 2007 recherche uniquement le groupe de macros de ce nom dans la base de données actuelle.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Texte de la barre d’état</strong></p></td>
<td><p>Texte à afficher dans la barre d’état lorsque le menu est sélectionné. Cet argument est ignoré pour les menus contextuels</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Pour exécuter l'action **AjouterMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **AddMenu** de l'objet **DoCmd**. Vous pouvez également définir la propriété **MenuBar** ou **ShortcutMenuBar** dans VBA pour créer un menu contextuel sous l'onglet **Compléments** ou pour attacher un menu contextuel personnalisé à un formulaire, un rapport ou un contrôle. Vous pouvez définir la propriété **ShortcutMenuBar** de l'objet **Application** pour créer un menu contextuel global.

