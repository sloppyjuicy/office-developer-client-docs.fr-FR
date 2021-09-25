---
title: Commandes de mise en forme en général
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 19717ba09664798c8e3ac73c2d03502ec2222620
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568466"
---
# <a name="shape-commands-in-general"></a>Commandes de mise en forme en général

**S’applique à** : Access 2013, Office 2013

La mise en forme des données définit les colonnes d'un objet **Recordset** mis en forme, la relation entre les entités représentées par les colonnes et la façon dont un objet **Recordset** est rempli avec des données.

Un objet **Recordset** mis en forme peut se composer des types de colonnes suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de colonne</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>data</p></td>
<td><p>Champs d’un objet <strong>Recordset</strong> retournés par une commande de requête à un fournisseur de données, une table ou un objet <strong>Recordset</strong> préalablement mis en forme.</p></td>
</tr>
<tr class="even">
<td><p>chapter</p></td>
<td><p>Référence à un autre objet <strong>Recordset</strong>, appelée <em>chapitre</em>. Les colonnes de chapitre permettent de définir une relation <em>parent-enfant</em> dans laquelle le <em>parent</em> est l'objet <strong>Recordset</strong> contenant la colonne de chapitre et l'<em>enfant</em> est l'objet <strong>Recordset</strong> représenté par le chapitre.</p></td>
</tr>
<tr class="odd">
<td><p>aggregate</p></td>
<td><p>La valeur de la colonne est obtenue par l’exécution d’une <em>fonction d’agrégation</em> sur toutes les lignes ou une colonne de toutes les lignes d’un objet <strong>Recordset</strong>.(Consultez la section relative aux fonctions d’agrégation dans la rubrique <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Fonctions d’agrégation, fonction CALC et mot clé NEW</a>.)</p></td>
</tr>
<tr class="even">
<td><p>expression calculée</p></td>
<td><p>La valeur de la colonne est obtenue par le calcul d’une expression Visual Basic pour Applications sur les colonnes d’une même ligne de l’objet <strong>Recordset</strong>.  L’expression est l’argument de la fonction CALC. (Consultez la section Expression calculée dans les rubriques<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Fonctions d’agrégation, fonction CALC et mot clé NEW</a> et <a href="visual-basic-for-applications-functions.md">Fonctions Visual Basic pour Applications</a>.)</p></td>
</tr>
<tr class="odd">
<td><p>Nouveau</p></td>
<td><p>Champs créés et vides qui peuvent être ultérieurement remplis avec des données. La colonne est définie avec le mot-clé NEW. (Voir la section consacrée au mot-clé NEW dans la rubrique <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Fonctions d’agrégation, fonction CALC et mot clé NEW</a>.)</p></td>
</tr>
</tbody>
</table>


Une commande SHAPE peut contenir une clause qui spécifie une commande de requête destinée à un fournisseur de données sous-jacent qui retournera un objet **Recordset**. La syntaxe de la requête dépend des exigences du fournisseur de données sous-jacent. Elle est en général écrite en langage SQL, même si ADO ne requiert pas de langage particulier.

Vous pouvez utiliser une clause JOIN SQL pour établir une relation entre deux tables ; cependant, sachez qu'un objet **Recordset** hiérarchique peut représenter les informations de manière plus efficace. Chaque ligne d'un objet **Recordset** créé par une clause JOIN reproduit les informations de l'une des tables de façon redondante. En revanche, un objet **Recordset** hiérarchique ne comporte qu'un objet **Recordset** parent pour chacun des différents objets **Recordset** enfant.

Les commandes SHAPE peuvent être émises par des objets **Recordset** ou en définissant la propriété [CommandText](commandtext-property-ado.md) de l'objet [Command](command-object-ado.md), puis en appelant la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

Elles peuvent être imbriquées. Cela signifie que *parent-command* ou *child-command* peut se trouver dans une autre commande SHAPE.

Le fournisseur de mise en forme retourne toujours un curseur client, même lorsque l'utilisateur spécifie **adUseServer** comme emplacement de curseur.

Pour plus d'informations sur la navigation au sein d'un objet **Recordset** hiérarchique, consultez [Accès aux lignes d'un jeu d'enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md).

Pour obtenir des informations détaillées sur la syntaxe des commandes SHAPE, consultez [Grammaire de mise en forme formelle](formal-shape-grammar.md).

## <a name="see-also"></a>Voir aussi

- [Issuing Commands to the Underlying Data Provider](issuing-commands-to-the-underlying-data-provider.md)

