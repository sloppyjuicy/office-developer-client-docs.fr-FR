---
title: ExécuterCommandeMenu, action de macro
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470982"
---
# <a name="runmenucommand-macro-action"></a>ExécuterCommandeMenu, action de macro


**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l'action **ExécuterCommandeMenu** pour exécuter une commande Microsoft Office Access.

## <a name="setting"></a>Valeur

L'action **ExécuterCommandeMenu** utilise l'argument d'action suivant :

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


## <a name="remarks"></a>Notes

Vous pouvez utiliser l'action **ExécuterCommandeMenu** pour exécuter une commande Access à partir d'une barre de menus personnalisée, d'une barre de menus globale, d'un menu contextuel personnalisé ou d'un menu contextuel global.

Vous pouvez utiliser l'action **ExécuterCommandeMenu** dans une macro avec des expressions conditionnelles pour exécuter une commande en fonction de certaines conditions.


> [!NOTE]
> <P>[!REMARQUE] Si vous cliquez sur l'onglet <STRONG>Fichier</STRONG>, puis sur <STRONG>Récent</STRONG>, les bases de données récemment utilisées s'affichent. Vous pouvez cliquer sur l'une de ces bases de données au lieu de cliquer sur <STRONG>Ouvrir</STRONG>. Ces éléments de base de données ne s'affichent pas dans la zone de liste déroulante de l'argument <STRONG>Commande</STRONG> et ne sont pas disponibles lorsque vous utilisez l'action <STRONG>ExécuterCommandeMenu</STRONG> dans une macro.</P>



Il se peut que certaines commandes ne soient plus disponibles lorsque vous convertissez une base de données créée avec une version précédente d'Access. Une commande peut avoir été renommée, transférée vers un autre menu ou n'existe peut-être plus dans Access. Les actions **ExécuterElémentMenu** pour de telles commandes ne peuvent pas être converties en actions **ExécuterCommandeMenu**. Lorsque vous ouvrez la macro, Access affichera une action **ExécuterCommandeMenu** avec un argument **Commande** vide pour ces commandes. Vous devez modifier la macro et entrer un argument Commande valide ou supprimer l'action **ExécuterCommandeMenu**.

Pour exécuter l'action **ExécuterCommandeMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RunCommand** de l'objet **Application**. (Elle correspond à la méthode **RunCommand** de l'objet **DoCmd**.)

