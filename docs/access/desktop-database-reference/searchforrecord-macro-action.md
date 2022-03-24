---
title: SearchForRecord, action de macro
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: de46fc102d1e7ce01fa0622a711f98673b82fba0
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63722418"
---
# <a name="searchforrecord-macro-action"></a>SearchForRecord, action de macro


**S’applique à** : Access 2013, Office 2013

L’action **RechercherEnregistrement** permet de rechercher un enregistrement spécifique dans une table, une requête, un formulaire ou un état.

## <a name="setting"></a>Setting

L’action **RechercherEnregistrement** accepte les arguments suivants.

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
<td><p><strong>Type d’objet</strong></p></td>
<td><p>Entrez ou sélectionnez le type d'objet de base de données dans lequel vous souhaitez effectuer votre recherche. Vous pouvez sélectionner <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong> ou <strong>État</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l'objet</strong></p></td>
<td><p>Entrez ou sélectionnez l'objet spécifique qui contient l'enregistrement à rechercher. La liste déroulante affiche tous les objets de base de données du type sélectionné pour l'argument <strong>Type d'objet</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Enregistrement</strong></p></td>
<td><p>Spécifiez le point de départ et la direction de la recherche.</p>
<div class="tableSection">
<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Setting</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Précédent</strong></p></td>
<td><p>Recherche en arrière à partir de l'enregistrement actif.</p></td>
</tr>
<tr class="even">
<td><p><strong>Suivant</strong></p></td>
<td><p>Recherche vers l'avant à partir de l'enregistrement actif.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Premier</strong></p></td>
<td><p>Recherche vers l'avant à partir du premier enregistrement. Il s'agit de la valeur par défaut pour cet argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Dernier</strong></p></td>
<td><p>Recherche en arrière à partir du dernier enregistrement.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Condition Where</strong></p></td>
<td><p>Entrez les critères de la recherche à l’aide de la même syntaxe qu’une clause WHERE SQL, uniquement sans le mot &quot;WHERE&quot;. Par exemple :</p>
<p>`Description = "Beverages"`</p>
<p>Pour créer un critère qui comprend une valeur dans une zone de texte d'un formulaire, vous devez créer une expression qui concatène la première partie du critère avec le nom de la zone de texte contenant la valeur à rechercher. Par exemple, le critère suivant recherche le champ Description de la valeur dans la zone de texte txtDescription du formulaire frmCategories. Notez le signe égal (<strong>=</strong>) au début de l’expression et l’utilisation de guillemets simples (') de part et <strong>d’autre</strong> de la référence de zone de texte :</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

- Lorsque plusieurs enregistrements correspondent aux critères dans l’argument **Condition Where**, les facteurs suivants déterminent l’enregistrement trouvé :
    
  - **La définition de l’argument Record** Voir la table dans la section Paramètres pour plus d’informations sur l’argument **Record**.
    
  - **L’ordre de tri des enregistrements** Par exemple, si l’argument **Record** est défini sur **First**, le fait de changer l’ordre de tri des enregistrements peut permettre de trouver un autre enregistrement.

- Vous devez ouvrir l'objet spécifié dans l'argument **Nom de l'objet** avant d'exécuter cette action. Sinon, une erreur se produit.

- Si les critères de l'argument **Condition Where** ne sont pas remplis, aucune erreur ne se produit et le focus reste sur l'enregistrement actif.

- Si vous recherchez l'enregistrement suivant ou précédent, la recherche s'arrête lorsqu'elle atteint la fin des données. Si aucun autre enregistrement ne correspond aux critères, aucune erreur ne se produit et le focus reste sur l'enregistrement actif. Pour confirmer qu'un enregistrement a été trouvé, entrez une condition pour l'action suivante, en faisant en sorte que la condition soit la même que les critères de l'argument **Condition Where**.

- Pour exécuter l'action **RechercherEnregistrement** dans un module VBA, utilisez la méthode **RechercherEnregistrement** de l'objet **DoCmd**.

- L'action **RechercherEnregistrement** est similaire à l'action **[TrouverEnregistrement](findrecord-macro-action.md)**, à la différence près que **RechercherEnregistrement** comporte des fonctionnalités de recherche plus puissantes. L'action **RechercherEnregistrement** est essentiellement destinée à la recherche de chaînes et elle reproduit la fonctionnalité de la boîte de dialogue **Rechercher**. L'action **RechercherEnregistrement** utilise des critères similaires à ceux d'un filtre ou d'une requête SQL. La liste ci-après illustre certaines opérations que vous pouvez effectuer à l'aide de l'action **RechercherEnregistrement**:
    
  - Vous pouvez utiliser des critères complexes dans l'argument **Condition Where**, tels que :
        
    `Description = "Beverages" and CategoryID = 11`
    
  - Vous pouvez faire référence à des champs qui se trouvent dans la source d’enregistrement d’un formulaire ou d’un état mais qui n’apparaissent pas dans le formulaire ou l’état. Dans l’exemple précédent, ni Description ni CategoryID ne doivent apparaître dans le formulaire ou l’état pour que les critères fonctionnent.
    
  - Vous pouvez utiliser des opérateurs logiques, tels **\<**, **\>** que , **AND**, **OR** et **BETWEEN**. L’action **TrouverEnregistrement** ne produit que des résultats qui sont égaux à, commencent par ou contiennent la chaîne recherchée.

## <a name="example"></a>Exemple

La macro suivante ouvre d’abord la table Catégories en utilisant l’action **OuvrirTable**. Elle utilise ensuite l’action **RechercherEnregistrement** pour rechercher le premier enregistrement dans la table pour lequel le champ Description correspond à « Boissons ».

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Action</p></th>
<th><p>Arguments</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>OpenTable</strong></p></td>
<td><p><strong>Nom de la</strong> table : <strong>CategoriesView</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>SearchForRecord</strong></p></td>
<td><p><strong>Type d’objet</strong> <strong>: TableObject Name</strong>: <strong>CategoriesRecord</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Où&quot;</p></td>
</tr>
</tbody>
</table>

