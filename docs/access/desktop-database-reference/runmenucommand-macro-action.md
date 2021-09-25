---
title: RunMenuCommand, action de macro
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 405d2d69666f6ebe9065ea6656e3fe1b4192153b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562243"
---
# <a name="runmenucommand-macro-action"></a>RunMenuCommand, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **ExécuterCommandeMenu** pour exécuter une commande Microsoft Office Access.

## <a name="setting"></a>Paramètre

L’action **ExécuterCommandeMenu** utilise l’argument d’action suivant :

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
<td><p><strong>Command</strong></p></td>
<td><p>Nom de la commande à exécuter. La zone <strong>Commande</strong> affiche les commandes intégrées disponibles dans Access et classées par ordre alphabétique. Cet argument est obligatoire.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’action **ExécuterCommandeMenu** pour exécuter une commande Access à partir d’une barre de menus personnalisée, d’une barre de menus globale, d’un menu contextuel personnalisé ou d’un menu contextuel global.

Vous pouvez utiliser l'action **ExécuterCommandeMenu** dans une macro avec des expressions conditionnelles pour exécuter une commande en fonction de certaines conditions.

> [!NOTE]
> [!REMARQUE] Si vous cliquez sur l'onglet **Fichier**, puis sur **Récent**, les bases de données récemment utilisées s'affichent. Vous pouvez cliquer sur l'une de ces bases de données au lieu de cliquer sur **Ouvrir**. Ces éléments de base de données ne s'affichent pas dans la zone de liste déroulante de l'argument **Commande** et ne sont pas disponibles lorsque vous utilisez l'action **ExécuterCommandeMenu** dans une macro.

Il se peut que certaines commandes ne soient plus disponibles lorsque vous convertissez une base de données créée avec une version précédente d'Access. Une commande peut avoir été renommée, transférée vers un autre menu ou n'existe peut-être plus dans Access. Les actions **ExécuterElémentMenu** pour de telles commandes ne peuvent pas être converties en actions **ExécuterCommandeMenu**. Lorsque vous ouvrez la macro, Access affichera une action **ExécuterCommandeMenu** avec un argument **Commande** vide pour ces commandes. Vous devez modifier la macro et entrer un argument Commande valide ou supprimer l'action **ExécuterCommandeMenu**.

Pour exécuter l'action **ExécuterCommandeMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RunCommand** de l'objet **Application**. (Elle correspond à la méthode **RunCommand** de l'objet **DoCmd**.)

