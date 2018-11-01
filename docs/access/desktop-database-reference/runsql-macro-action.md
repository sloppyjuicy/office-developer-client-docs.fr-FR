---
title: ExécuterSQL, action de macro
TOCTitle: RunSQL Macro Action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c5fd5bea659b3df368f6e352d0ae233b5e066113
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875594"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="6a4c4-102">ExécuterSQL, action de macro</span><span class="sxs-lookup"><span data-stu-id="6a4c4-102">RunSQL Macro Action</span></span>


<span data-ttu-id="6a4c4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a4c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a4c4-p101">Vous pouvez utiliser l'action **ExécuterSQL** pour exécuter une requête Action Access en utilisant l'instruction SQL correspondante. Vous pouvez également utiliser une requête Définition des données.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p101">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement. You can also run a data-definition query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6a4c4-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="6a4c4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a4c4-108">Setting</span></span>

<span data-ttu-id="6a4c4-109">L'action **ExécuterSQL** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-109">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a4c4-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="6a4c4-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6a4c4-111">Description</span><span class="sxs-lookup"><span data-stu-id="6a4c4-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-112"><strong>Instruction SQL</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c4-112"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c4-p103">Instruction SQL pour la requête Action ou Définition des données que vous souhaitez exécuter. L'instruction peut compter au maximum 255 caractères. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p103">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c4-116"><strong>Utilise la transaction</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c4-116"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c4-p104">Sélectionnez <strong>Oui</strong> pour inclure cette requête dans une transaction. Choisissez <strong>Non</strong> si vous ne souhaitez pas utiliser de transaction. La valeur par défaut est <strong>Oui</strong>. Si vous sélectionnez la valeur <strong>Non</strong> pour cet argument, l'exécution de la requête peut être plus rapide.  </span><span class="sxs-lookup"><span data-stu-id="6a4c4-p104">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6a4c4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6a4c4-121">Remarks</span></span>

<span data-ttu-id="6a4c4-p105">Vous pouvez utiliser des requêtes Action pour ajouter, supprimer ou mettre à jour des enregistrements et pour enregistrer le jeu de résultats d'une requête en tant que nouvelle table. Vous pouvez utiliser des requêtes Définition des données pour créer, modifier et supprimer des tables ou encore pour créer et supprimer des index. Avec l'action **ExécuterSQL**, vous pouvez effectuer ces opérations directement à partir d'une macro sans devoir utiliser les requêtes stockées.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p105">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="6a4c4-p106">Si vous devez spécifier une instruction SQL comportant plus de 255 caractères, utilisez plutôt la méthode **RunSQL** de l'objet **DoCmd** dans un module Visual Basic pour Applications (VBA). Vous pouvez taper des instructions SQL comptant jusqu'à 32 768 caractères dans VBA.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p106">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="6a4c4-p107">Les requêtes Access sont en fait des instructions SQL créées lorsque vous créez une requête à l'aide de la grille de création dans la fenêtre Requête. Le tableau suivant répertorie les requêtes Action et Définition des données d'Access et leurs instructions SQL correspondantes.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p107">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a4c4-129">Type de requête</span><span class="sxs-lookup"><span data-stu-id="6a4c4-129">Query type</span></span></p></th>
<th><p><span data-ttu-id="6a4c4-130">Instruction SQL</span><span class="sxs-lookup"><span data-stu-id="6a4c4-130">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-131"><strong>Action</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c4-131"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c4-132">Ajout</span><span class="sxs-lookup"><span data-stu-id="6a4c4-132">Append</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-133">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="6a4c4-133">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-134">Suppression</span><span class="sxs-lookup"><span data-stu-id="6a4c4-134">Delete</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="6a4c4-135">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c4-136">Création de table</span><span class="sxs-lookup"><span data-stu-id="6a4c4-136">Make-table</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-137">SÉLECTIONNEZ... DANS</span><span class="sxs-lookup"><span data-stu-id="6a4c4-137">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-138">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="6a4c4-138">Update</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-139">UPDATE</span><span class="sxs-lookup"><span data-stu-id="6a4c4-139">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c4-140"><strong>Définition de données (spécifique SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c4-140"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-141">Créer une table</span><span class="sxs-lookup"><span data-stu-id="6a4c4-141">Create a table</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-142">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="6a4c4-142">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c4-143">Modifier une table</span><span class="sxs-lookup"><span data-stu-id="6a4c4-143">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-144">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="6a4c4-144">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-145">Supprimer une table</span><span class="sxs-lookup"><span data-stu-id="6a4c4-145">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-146">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="6a4c4-146">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c4-147">Créer un index</span><span class="sxs-lookup"><span data-stu-id="6a4c4-147">Create an index</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-148">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="6a4c4-148">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c4-149">Supprimer un index</span><span class="sxs-lookup"><span data-stu-id="6a4c4-149">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="6a4c4-150">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="6a4c4-150">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a4c4-151">Vous pouvez également utiliser une clause IN avec ces instructions pour modifier des données dans une autre base de données.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-151">You can also use an IN clause with these statements to modify data in another database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6a4c4-p108">[!REMARQUE] Pour exécuter une requête Sélection ou une requête Analyse croisée à partir d'une macro, utilisez l'argument Affichage de l'action <STRONG>OuvrirRequête</STRONG> pour ouvrir une requête Sélection ou Analyse croisée existante en mode Feuille de données. Vous pouvez également exécuter des requêtes Action et des requêtes spécifiques SQL existantes de la même façon.</span><span class="sxs-lookup"><span data-stu-id="6a4c4-p108">To run a select query or crosstab query from a macro, use the View argument of the <STRONG>OpenQuery</STRONG> action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span></P>


