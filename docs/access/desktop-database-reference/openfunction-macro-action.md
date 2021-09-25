---
title: OpenFunction, action de macro
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d083336e4a67188d654bb95a585c898cde3b112f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617908"
---
# <a name="openfunction-macro-action"></a>OpenFunction, action de macro

**S’applique à** : Access 2013, Office 2013

Dans un projet Access, vous pouvez utiliser l'action **OuvrirFonction** pour ouvrir une fonction définie par l'utilisateur en mode Feuille de données, une fonction en ligne en mode Création, l'Éditeur de texte SQL (pour une fonction scalaire ou une fonction tabulaire définie par l'utilisateur) ou un Aperçu avant impression. Cette action exécute la fonction définie par l'utilisateur lorsqu'elle est ouverte en mode Feuille de données. Vous pouvez également sélectionner le mode de saisie de données pour la fonction définie par l'utilisateur et limiter les enregistrements que celle-ci affiche.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **OuvrirFonction** possède les arguments suivants.

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
<td><p><strong>Nom de la fonction</strong></p></td>
<td><p>Nom de la fonction définie par l’utilisateur à ouvrir. La zone <strong>Nom de la fonction</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro affiche toutes les fonctions définies par l’utilisateur dans la base de données active. Il s’agit d’un argument obligatoire. Si vous exécutez <strong></strong> une macro contenant l’action Fonction dans une base de données bibliothèque, Microsoft Access recherche d’abord la fonction de ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Affichage dans lequel s’ouvre la fonction définie par l’utilisateur. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mode Données</strong></p></td>
<td><p>Mode de saisie de données de la fonction définie par l’utilisateur. S’applique uniquement aux fonctions définies par l’utilisateur ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut ni afficher ni modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut afficher et modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette action équivaut à double-cliquer sur une fonction définie par l’utilisateur dans le volet de navigation ou à cliquer avec le bouton droit sur la fonction dans le volet de navigation et à choisir un affichage.

Basculer en mode Création lorsque la fonction définie par l'utilisateur est ouverte supprime le paramètre de l'argument **Mode Données** de la fonction. Ce paramètre n'est pas actif, même si l'utilisateur revient en mode Feuille de données.

> [!TIP]
> - Vous pouvez sélectionner une fonction définie par l'utilisateur dans le volet de navigation et la faire glisser vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirFonction** qui ouvre la fonction définie par l'utilisateur en mode Feuille de données.
> - Si vous ne voulez pas afficher les messages système qui s'affichent normalement lorsqu'une fonction définie par l'utilisateur est exécutée (indiquant qu'il s'agit d'une fonction définie par l'utilisateur et affichant le nombre d'enregistrements concernés), vous pouvez faire appel à l'action **Avertissements** pour supprimer l'affichage de ces messages.

Pour exécuter l'action **OuvrirFonction** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenFunction** de l'objet **DoCmd**.

