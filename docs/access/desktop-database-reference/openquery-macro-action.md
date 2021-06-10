---
title: OpenQuery, action de macro
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288342"
---
# <a name="openquery-macro-action"></a>OpenQuery, action de macro

**S’applique à** : Access 2013, Office 2013

Faites appel à l'action **OuvrirRequête** pour ouvrir une requête Sélection ou Analyse croisée en mode Feuille de données, Création ou Aperçu avant impression. Cette action exécute une requête Action. Vous pouvez également sélectionner le mode de saisie des données voulu pour la requête.

> [!NOTE]
> [!REMARQUE] Cette action n'est disponible que dans l'environnement de base de données Access (.mdb ou .accdb). Reportez-vous aux actions **OuvrirVue**, **OuvrirProcédureStockée** ou **OuvrirFonction** si vous utilisez l'environnement de projet Access (.adp).

## <a name="setting"></a>Paramètre

L’action **OuvrirRequête** possède les arguments suivants.

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
<td><p><strong>Nom de la requête</strong></p></td>
<td><p>Nom de la requête à ouvrir. La <strong>zone Nom de la</strong> requête dans la section Arguments de l’action du volet Générateur de macro affiche toutes les requêtes de la base de données actuelle. <strong></strong> Il s’agit d’un argument obligatoire. Si vous exécutez <strong></strong> une macro contenant l’action OuvrirRequête dans une base de données bibliothèque, Microsoft Access recherche d’abord la requête de ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Affichage dans lequel s’ouvre la requête. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mode Données</strong></p></td>
<td><p>Mode de saisie de données de la requête. S’applique uniquement aux requêtes ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut pas modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si l’argument **Affichage** a la valeur **Feuille de données**, Access affiche le jeu de résultats si la requête est une requête Sélection, Analyse croisée, Union ou SQL direct dont la propriété **RenvoieSur** a la valeur **Oui** ; et renvoie la requête s’il s’agit d’une requête Action, Définition des données ou SQL direct dont la propriété **RenvoieSur** a la valeur **Non**.

L'action **OuvrirRequête** équivaut à double-cliquer sur la requête dans le volet de navigation ou à cliquer avec le bouton droit sur la requête dans le volet de navigation et à choisir un affichage. Cette action vous permet de sélectionner des options supplémentaires.

> [!TIP]
> - Vous pouvez faire glisser une requête depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirRequête** qui ouvre la requête en mode Feuille de données. Basculer en mode Création lorsque la requête est ouverte supprime le paramètre de l'argument **Mode Données** de la requête. Ce paramètre n'est pas actif, même si l'utilisateur revient en mode Feuille de données.
> - Si vous ne voulez pas afficher les messages système qui s'affichent normalement lorsqu'une requête d'action est exécutée (indiquant qu'il s'agit d'une requête d'action et affichant le nombre d'enregistrements concernés), vous pouvez faire appel à l'action **Avertissements** pour supprimer l'affichage de ces messages.

Pour exécuter l'action **OuvrirRequête** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenQuery** de l'objet **DoCmd**.

