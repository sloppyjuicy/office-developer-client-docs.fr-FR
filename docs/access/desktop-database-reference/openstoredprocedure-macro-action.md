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
ms.openlocfilehash: 22d3422a5c00e6caa20003df3574c26ab061ab53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925344"
---
# <a name="openstoredprocedure-macro-action"></a>OpenStoredProcedure, action de macro


**S’applique à**: Access 2013, Office 2013

Dans un projet Access, vous pouvez utiliser l’action **OuvrirProcédureStockée** pour ouvrir une procédure stockée en mode Feuille de données, Création de procédure stockée ou Aperçu avant impression. Cette action exécute la procédure stockée nommée lorsqu’elle est ouverte en mode Feuille de données. Vous pouvez choisir le mode de saisie des données voulu pour la procédure stockée et limiter les enregistrements que celle-ci affiche.


> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Paramètre

L’action **OuvrirProcédureStockée** possède les arguments suivants.

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
<td><p><strong>Nom de la procédure</strong></p></td>
<td><p>Nom de la procédure stockée à ouvrir. La zone <strong>Nom procédure dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro</strong> affiche toutes les procédures stockées dans la base de données en cours. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>OuvrirProcédureStockée</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord la procédure stockée portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
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


## <a name="remarks"></a>Notes

Cette action équivaut à double-cliquer sur la procédure stockée dans le volet de navigation ou à cliquer avec le bouton droit sur la procédure stockée dans le volet de navigation, puis à sélectionner la commande de votre choix.

Basculer en mode Création lorsque la procédure stockée est ouverte supprime le paramètre de l’argument **Mode Données** de la procédure stockée. Ce paramètre n’est pas actif, même si l’utilisateur revient en mode Feuille de données.


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P>Vous pouvez faire glisser une procédure stockée à partir du volet de Navigation vers une ligne d’action de macro. Cette opération crée automatiquement une action <STRONG>OuvrirProcédureStockée</STRONG> qui ouvre la procédure stockée en mode feuille de données.</P>
> <LI>
> <P>
> 						Si vous ne voulez pas afficher les messages système qui s’affichent normalement lorsqu’une procédure stockée est exécutée (indiquant qu’il s’agit d’une procédure stockée et affichant le nombre d’enregistrements concernés), vous pouvez faire appel à l’action <STRONG>Avertissements</STRONG> pour supprimer l’affichage de ces messages.
</P></LI></UL>
<P></P>



Pour exécuter l’action **OuvrirProcédureStockée** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenStoredProcedure** de l’objet **DoCmd**.

