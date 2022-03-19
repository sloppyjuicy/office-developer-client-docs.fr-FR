---
title: OpenStoredProcedure, action de macro
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7a4e88e622c15517dd8222a6bfbf207259790bcd
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628200"
---
# <a name="openstoredprocedure-macro-action"></a>OpenStoredProcedure, action de macro

**S’applique à** : Access 2013, Office 2013

Dans un projet Access, vous pouvez utiliser l’action **OuvrirProcédureStockée** pour ouvrir une procédure stockée en mode Feuille de données, Création de procédure stockée ou Aperçu avant impression. Cette action exécute la procédure stockée nommée lorsqu’elle est ouverte en mode Feuille de données. Vous pouvez choisir le mode de saisie des données voulu pour la procédure stockée et limiter les enregistrements que celle-ci affiche.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **OuvrirProcédureStockée** possède les arguments suivants.

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
<td><p><strong>Nom de la procédure</strong></p></td>
<td><p>Nom de la procédure stockée à ouvrir. La <strong>zone Nom de</strong> la procédure de la section <strong>Arguments de l’action</strong> du volet Générateur de macro affiche toutes les procédures stockées dans la base de données actuelle. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>OuvrirProcédureStockée</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord la procédure stockée portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Affichage dans lequel s’ouvre la procédure stockée. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mode Données</strong></p></td>
<td><p>Mode de saisie de données de la procédure stockée. S’applique uniquement aux procédures stockées ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut ni afficher ni modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut afficher et modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Cette action équivaut à double-cliquer sur la procédure stockée dans le volet de navigation ou à cliquer avec le bouton droit sur la procédure stockée dans le volet de navigation, puis à sélectionner la commande de votre choix.

Basculer en mode Création lorsque la procédure stockée est ouverte supprime le paramètre de l’argument **Mode Données** de la procédure stockée. Ce paramètre n’est pas actif, même si l’utilisateur revient en mode Feuille de données.

> [!TIP]
> - Vous pouvez faire glisser une procédure stockée du volet de navigation vers une ligne d’action de macro. Ceci crée automatiquement une action **OuvrirProcédureStockée** qui ouvre la procédure stockée en mode Feuille de données.
> - Si vous ne voulez pas afficher les messages système qui s’affichent normalement lorsqu’une procédure stockée est exécutée (indiquant qu’il s’agit d’une procédure stockée et affichant le nombre d’enregistrements concernés), vous pouvez faire appel à l’action **Avertissements** pour supprimer l’affichage de ces messages.

Pour exécuter l’action **OuvrirProcédureStockée** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenStoredProcedure** de l’objet **DoCmd**.

