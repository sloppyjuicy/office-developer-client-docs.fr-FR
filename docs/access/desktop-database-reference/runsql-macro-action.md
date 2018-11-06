---
title: RunSQL, action de macro
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0527f5a55235fa36725152d228dfd2294c63bf53
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996873"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="d0bf1-102">RunSQL, action de macro</span><span class="sxs-lookup"><span data-stu-id="d0bf1-102">RunSQL macro action</span></span>

<span data-ttu-id="d0bf1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0bf1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0bf1-p101">Vous pouvez utiliser l'action **ExécuterSQL** pour exécuter une requête Action Access en utilisant l'instruction SQL correspondante. Vous pouvez également utiliser une requête Définition des données.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-p101">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement. You can also run a data-definition query.</span></span>

> [!NOTE]
> <span data-ttu-id="d0bf1-106">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d0bf1-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0bf1-107">Setting</span></span>

<span data-ttu-id="d0bf1-108">L'action **ExécuterSQL** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-108">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0bf1-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d0bf1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d0bf1-110">Description</span><span class="sxs-lookup"><span data-stu-id="d0bf1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-111"><strong>Instruction SQL</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf1-111"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bf1-p102">Instruction SQL pour la requête Action ou Définition des données que vous souhaitez exécuter. L'instruction peut compter au maximum 255 caractères. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-p102">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf1-115"><strong>Utilise la transaction</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf1-115"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bf1-p103">Sélectionnez <strong>Oui</strong> pour inclure cette requête dans une transaction. Choisissez <strong>Non</strong> si vous ne souhaitez pas utiliser de transaction. La valeur par défaut est <strong>Oui</strong>. Si vous sélectionnez la valeur <strong>Non</strong> pour cet argument, l'exécution de la requête peut être plus rapide.  </span><span class="sxs-lookup"><span data-stu-id="d0bf1-p103">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d0bf1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d0bf1-120">Remarks</span></span>

<span data-ttu-id="d0bf1-p104">Vous pouvez utiliser des requêtes Action pour ajouter, supprimer ou mettre à jour des enregistrements et pour enregistrer le jeu de résultats d'une requête en tant que nouvelle table. Vous pouvez utiliser des requêtes Définition des données pour créer, modifier et supprimer des tables ou encore pour créer et supprimer des index. Avec l'action **ExécuterSQL**, vous pouvez effectuer ces opérations directement à partir d'une macro sans devoir utiliser les requêtes stockées.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-p104">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="d0bf1-p105">Si vous devez spécifier une instruction SQL comportant plus de 255 caractères, utilisez plutôt la méthode **RunSQL** de l'objet **DoCmd** dans un module Visual Basic pour Applications (VBA). Vous pouvez taper des instructions SQL comptant jusqu'à 32 768 caractères dans VBA.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-p105">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="d0bf1-p106">Les requêtes Access sont en fait des instructions SQL créées lorsque vous créez une requête à l'aide de la grille de création dans la fenêtre Requête. Le tableau suivant répertorie les requêtes Action et Définition des données d'Access et leurs instructions SQL correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-p106">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0bf1-128">Type de requête</span><span class="sxs-lookup"><span data-stu-id="d0bf1-128">Query type</span></span></p></th>
<th><p><span data-ttu-id="d0bf1-129">Instruction SQL</span><span class="sxs-lookup"><span data-stu-id="d0bf1-129">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-130"><strong>Action</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf1-130"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf1-131">Ajout</span><span class="sxs-lookup"><span data-stu-id="d0bf1-131">Append</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-132">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="d0bf1-132">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-133">Suppression</span><span class="sxs-lookup"><span data-stu-id="d0bf1-133">Delete</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="d0bf1-134">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf1-135">Création de table</span><span class="sxs-lookup"><span data-stu-id="d0bf1-135">Make-table</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-136">SÉLECTIONNEZ... DANS</span><span class="sxs-lookup"><span data-stu-id="d0bf1-136">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-137">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="d0bf1-137">Update</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-138">UPDATE</span><span class="sxs-lookup"><span data-stu-id="d0bf1-138">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf1-139"><strong>Définition de données (spécifique SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf1-139"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-140">Créer une table</span><span class="sxs-lookup"><span data-stu-id="d0bf1-140">Create a table</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-141">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="d0bf1-141">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf1-142">Modifier une table</span><span class="sxs-lookup"><span data-stu-id="d0bf1-142">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-143">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="d0bf1-143">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-144">Supprimer une table</span><span class="sxs-lookup"><span data-stu-id="d0bf1-144">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-145">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="d0bf1-145">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf1-146">Créer un index</span><span class="sxs-lookup"><span data-stu-id="d0bf1-146">Create an index</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-147">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="d0bf1-147">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bf1-148">Supprimer un index</span><span class="sxs-lookup"><span data-stu-id="d0bf1-148">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="d0bf1-149">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="d0bf1-149">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d0bf1-150">Vous pouvez également utiliser une clause IN avec ces instructions pour modifier des données dans une autre base de données.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-150">You can also use an IN clause with these statements to modify data in another database.</span></span>

> [!NOTE]
> <span data-ttu-id="d0bf1-p107">[!REMARQUE] Pour exécuter une requête Sélection ou une requête Analyse croisée à partir d'une macro, utilisez l'argument Affichage de l'action **OuvrirRequête** pour ouvrir une requête Sélection ou Analyse croisée existante en mode Feuille de données. Vous pouvez également exécuter des requêtes Action et des requêtes spécifiques SQL existantes de la même façon.</span><span class="sxs-lookup"><span data-stu-id="d0bf1-p107">To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span>
