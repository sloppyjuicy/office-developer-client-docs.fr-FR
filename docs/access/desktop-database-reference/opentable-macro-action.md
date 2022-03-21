---
title: OpenTable, action de macro
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0c98dd666a941bc69d1c6d65412da9020b180fe3
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630594"
---
# <a name="opentable-macro-action"></a>OpenTable, action de macro

**S’applique à** : Access 2013, Office 2013

Faites appel à l'action **OuvrirTable** pour ouvrir une table en mode Feuille de données, Création ou Aperçu avant impression. Vous pouvez également sélectionner le mode de saisie des données voulu pour la table.

## <a name="setting"></a>Paramètres

L’action **OuvrirTable** possède les arguments suivants.

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
<td><p><strong>Nom de la table</strong></p></td>
<td><p>Nom de la table à ouvrir. La zone <strong>Nom de la table</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro affiche toutes les tables de la base de données active. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>OuvrirTable</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord la table portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Affichage dans lequel s’ouvre la table. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mode Données</strong></p></td>
<td><p>Mode de saisie de données de la table. S’applique uniquement aux tables ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut pas modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Cette action équivaut à double-cliquer sur la table dans le volet de navigation ou à cliquer dessus avec le bouton droit dans le volet de navigation, puis à choisir un affichage.

> [!TIP]
> [!CONSEIL] Vous pouvez faire glisser une table depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirTable** qui ouvre la table en mode Feuille de données.

Pour exécuter l'action **OuvrirTable** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenTable** de l'objet **DoCmd**.

