---
title: AjouterMenu, action de macro
TOCTitle: AddMenu Macro Action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 984b10638ab7f01aeb4dc9656bc70aa1e44d56a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471392"
---
# <a name="addmenu-macro-action"></a>AjouterMenu, action de macro


**S’applique à**: Access 2013 | Office 2013

Cet article décrit le fonctionnement de base de l'action de macro **AjouterMenu**.

Vous pouvez utiliser l'action **AjouterMenu** pour créer les éléments suivants :

- des menus personnalisés sous l'onglet **Compléments** d'un formulaire ou d'un état particulier ;

- un menu contextuel personnalisé pour un formulaire, un état ou un contrôle. Le menu contextuel personnalisé remplace le menu contextuel intégré pour le formulaire, l'état ou le contrôle ;

- un menu contextuel global. Le menu contextuel global remplace le menu contextuel intégré pour les champs des feuilles de données de table et de requête, des formulaires et des états, sauf là où vous avez ajouté un menu contextuel personnalisé pour un formulaire, un état ou un contrôle.

## <a name="setting"></a>Valeur

L'action **AjouterMenu** possède les arguments suivants.

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
<td><p>Le nom du menu, par exemple, &quot;rapport commandes&quot; ou &quot;outils&quot;. Pour créer une touche d’accès afin que vous puissiez utiliser le clavier pour choisir le menu, tapez un « et commercial » (<strong>&amp;</strong>) avant la lettre que vous voulez être la touche d’accès. Cette lettre sera soulignée dans le nom du menu dans l’onglet <strong>Compléments</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de la macro de menu</strong></p></td>
<td><p>Nom du groupe de macros qui contient les macros pour les commandes du menu. Cet argument est obligatoire. 

</p>

> [!NOTE]
> Si vous exécutez une macro contenant l’action **AjouterMenu** dans une base de données bibliothèque, Microsoft Office Access 2007 recherche le groupe de macros portant ce nom uniquement dans la base de données active.


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>Texte de la barre d’état</strong></p></td>
<td><p>Texte à afficher dans la barre d’état lorsque le menu est sélectionné. Cet argument est ignoré pour les menus contextuels</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Pour exécuter l'action **AjouterMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **AddMenu** de l'objet **DoCmd**. Vous pouvez également définir la propriété **MenuBar** ou **ShortcutMenuBar** dans VBA pour créer un menu contextuel sous l'onglet **Compléments** ou pour attacher un menu contextuel personnalisé à un formulaire, un rapport ou un contrôle. Vous pouvez définir la propriété **ShortcutMenuBar** de l'objet **Application** pour créer un menu contextuel global.

