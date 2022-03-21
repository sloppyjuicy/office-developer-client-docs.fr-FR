---
title: OpenView, action de macro
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0eb71be1f3402f1fa57fb96154beefcf7aae7985
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632041"
---
# <a name="openview-macro-action"></a>OpenView, action de macro

**S’applique à** : Access 2013, Office 2013

Dans un projet Access, vous pouvez utiliser l'action **OuvrirVue** pour ouvrir une vue en mode Feuille de données, Création ou Aperçu avant impression. Cette action exécute la vue nommée lorsqu'elle est ouverte en mode Feuille de données. Vous pouvez choisir le mode de saisie des données voulu pour la vue et limiter les enregistrements que celle-ci affiche.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **OuvrirVue** possède les arguments suivants.

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
<td><p><strong>Nom de la vue</strong></p></td>
<td><p>Nom de la vue à ouvrir. La <strong>zone Nom de</strong> l’affichage dans la section <strong>Arguments de l’action</strong> du volet Générateur de macro affiche tous les affichages de la base de données actuelle. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>OuvrirVue</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord la vue portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Affichage dans lequel s’ouvre la vue. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mode Données</strong></p></td>
<td><p>Mode de saisie de données de la vue. S’applique uniquement aux vues ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut ni afficher ni modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut afficher et modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette action équivaut à double-cliquer sur une vue dans le volet de navigation ou à cliquer avec le bouton droit sur la vue dans le volet de navigation, puis à sélectionner la commande de votre choix.

> [!TIP]
> - Vous pouvez faire glisser une vue depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirVue** qui ouvre la vue en mode Feuille de données.
> - Si vous ne voulez pas afficher les messages système qui s'affichent normalement lorsqu'une vue est exécutée (indiquant qu'il s'agit d'une vue et affichant le nombre d'enregistrements concernés), vous pouvez faire appel à l'action **Avertissements** pour supprimer l'affichage de ces messages.

Pour exécuter l'action **OuvrirVue** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenView** de l'objet **DoCmd**.

