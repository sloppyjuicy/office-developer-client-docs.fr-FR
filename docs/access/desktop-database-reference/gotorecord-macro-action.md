---
title: GoToRecord, action de macro
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292138"
---
# <a name="gotorecord-macro-action"></a>GoToRecord, action de macro


**S’applique à** : Access 2013, Office 2013

Utilisez l’action **AtteindreEnregistrement** pour que l’enregistrement spécifié devienne l’enregistrement actif dans le jeu de résultats d’une requête, d’une table ou d’un formulaire ouvert.

## <a name="setting"></a>Paramètre

L’action **AtteindreEnregistrement** possède les arguments suivants.

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
<td><p><strong>Type d’objet</strong></p></td>
<td><p>Type d’objet qui contient l’enregistrement que vous souhaitez rendre actif. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>Vue serveur</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide pour sélectionner l’objet actif.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet</strong></p></td>
<td><p>Nom de l’objet qui contient l’enregistrement que vous souhaitez rendre actif. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données active correspondant au type sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez également celui-ci vide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Enregistrement que vous souhaitez rendre actif. Cliquez sur <strong>Précédent</strong>, <strong>Suivant</strong>, <strong>Premier</strong>, <strong>Dernier</strong>, <strong>Atteindre</strong> ou <strong>Nouveau</strong> dans la zone <strong>Enregistrement</strong>. La valeur par défaut est <strong>Suivant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Entier ou expression qui correspond à un entier. Une expression doit être précédée d’un signe égal ( <strong>=</strong> ). Cet argument spécifie l’enregistrement à rendre actif. Vous pouvez utiliser l’argument <strong>Référence</strong> de deux manières :</p>
<ul>
<li><p>Lorsque l’argument <strong>Enregistrement</strong> a la valeur <strong>Suivant</strong> ou <strong>Précédent</strong>, Microsoft Office Access 2007 avance ou recule du nombre d’enregistrements spécifié dans l’argument <strong>Référence</strong>.</p></li>
<li><p>Lorsque l’argument <strong>Enregistrement</strong> est défini sur <strong>Atteindre</strong>, Access accède à l’enregistrement dont le numéro est égal à la valeur de l’argument <strong>Référence</strong>. Le numéro de l’enregistrement est indiqué dans la zone de numéro d’enregistrement en bas de la fenêtre.</p>
<p><strong>REMARQUE</strong>: si vous utilisez le <strong></strong> paramètre <strong>Premier,</strong> <strong>Dernier</strong>ou Nouveau pour l’argument <strong>Enregistrement,</strong> Access ignore l’argument <strong>Offset.</strong> Si vous entrez une valeur trop élevée pour l’argument <strong>Référence</strong>, Access affiche un message d’erreur. Vous ne pouvez pas entrer de nombres négatifs pour l’argument <strong>Référence</strong>.</p></li>
<li><p>Lorsque l’argument <strong>Enregistrement</strong> a la valeur <strong>Suivant</strong> ou <strong>Précédent</strong>, Microsoft Office Access 2007 avance ou recule du nombre d’enregistrements spécifié dans l’argument <strong>Référence</strong>.</p></li>
<li><p>Lorsque l’argument <strong>Enregistrement</strong> est défini sur <strong>Atteindre</strong>, Access accède à l’enregistrement dont le numéro est égal à la valeur de l’argument <strong>Référence</strong>. Le numéro de l’enregistrement est indiqué dans la zone de numéro d’enregistrement en bas de la fenêtre.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si un contrôle particulier d’un enregistrement a le focus, cette action laisse le focus dans le même contrôle pour le nouvel enregistrement.

Vous pouvez utiliser le paramètre **Nouveau** dans l'argument **Enregistrement** pour passer à l'enregistrement vide à la fin d'un formulaire ou d'une table de manière à pouvoir entrer de nouvelles données.

Cette action équivaut à cliquer sur la flèche sous le bouton **Rechercher** de l'onglet **Accueil**, puis à cliquer sur **Atteindre**. Les sous-commandes **Premier**, **Dernier**, **Suivant**, **Précédent** et **Nouvel enregistrement** de la commande **Atteindre** ont le même effet sur l'objet sélectionné que les paramètres **Premier**, **Dernier**, **Suivant**, **Précédent** et **Nouveau** de l'argument **Enregistrement**. Vous pouvez également atteindre des enregistrements en utilisant les boutons de navigation en bas de la fenêtre.

Vous pouvez utiliser l'action **AtteindreEnregistrement** pour rendre actif un enregistrement d'un formulaire masqué si vous spécifiez le formulaire masqué dans les arguments **Type d'objet** et **Nom de l'objet**.

Pour exécuter l'action **AtteindreEnregistrement** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToRecord** de l'objet **DoCmd**.

