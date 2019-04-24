---
title: Membres Recordset2 (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29d1472e8cd02d8968ba84dbc1c1cf99be7ee858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307272"
---
# <a name="recordset2-members-dao"></a><span data-ttu-id="2317b-102">Membres Recordset2 (DAO)</span><span class="sxs-lookup"><span data-stu-id="2317b-102">Recordset2 members (DAO)</span></span>


<span data-ttu-id="2317b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2317b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2317b-104">Un objet Recordset2 représente les enregistrements d'une table de base ou les enregistrements générés suite à l'exécution d'une requête.</span><span class="sxs-lookup"><span data-stu-id="2317b-104">A Recordset2 object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="2317b-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2317b-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2317b-106">Nom</span><span class="sxs-lookup"><span data-stu-id="2317b-106">Name</span></span></p></th>
<th><p><span data-ttu-id="2317b-107">Description</span><span class="sxs-lookup"><span data-stu-id="2317b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2317b-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-109">Crée un enregistrement pour un objet <strong>Recordset2</strong> modifiable.</span><span class="sxs-lookup"><span data-stu-id="2317b-109">Creates a new record for an updatable <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-111"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-111"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-112">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-113">Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-115">Annule les mises à jour en attente d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-117">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en double qui fait référence à l'objet <strong>Recordset2</strong> d'origine.</span><span class="sxs-lookup"><span data-stu-id="2317b-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-119">Ferme un objet <strong>Recordset</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="2317b-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-121">Renvoie un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong> qui est une copie de l'objet <strong>QueryDef</strong> utilisé pour créer l'objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> représenté par l'espace réservé Recordset (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2317b-122">.</span><span class="sxs-lookup"><span data-stu-id="2317b-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-124">Non prise en charge pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="2317b-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-126">Copie l'enregistrement actif d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> modifiable dans la mémoire tampon de la copie en vue d'une modification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2317b-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-128">Remplit tout ou partie d'un cache local pour un objet <strong>Recordset</strong> contenant les données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-130">Recherche le premier enregistrement dans un objet <strong>Recordset</strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-132">Recherche le dernier enregistrement dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-p103">Recherche l'enregistrement suivant dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-p104">Recherche l'enregistrement précédent dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-140">Extrait plusieurs lignes d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-142">Déplace l'enregistrement actif dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-143"><strong><a href="recordset2-movefirst-method-dao.md">Méthodes</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-144">Atteint le premier enregistrement d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2317b-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-146">Atteint le dernier enregistrement d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2317b-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-148">Atteint l'enregistrement suivant d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2317b-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-150">Atteint l'enregistrement précédent d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2317b-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-152"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-152"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-153">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-154">Obtient le jeu d'enregistrements suivant, le cas échéant, qui est renvoyé par une requête Sélection à parties multiples dans le cadre d'un appel <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong>, et renvoie une valeur de type <strong>Boolean</strong> indiquant si un ou plusieurs enregistrements supplémentaires sont en attente (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-156">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-157"><strong><a href="recordset2-requery-method-dao.md">Actualiser</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-158">Met à jour les données d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="2317b-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-160">Localise l’enregistrement dans un objet <strong>Recordset</strong> de type table indexé qui correspond aux critères spécifiés pour l’index actuel et fait de cet enregistrement l’enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-162"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-162"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-163">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-164">Enregistre le contenu de la mémoire tampon de la copie dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> modifiable.</span><span class="sxs-lookup"><span data-stu-id="2317b-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="2317b-165">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2317b-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2317b-166">Nom</span><span class="sxs-lookup"><span data-stu-id="2317b-166">Name</span></span></p></th>
<th><p><span data-ttu-id="2317b-167">Description</span><span class="sxs-lookup"><span data-stu-id="2317b-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2317b-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-169">Définit ou renvoie le nombre d’enregistrements relatif de l’enregistrement actif d’un objet <strong>Recordset2</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-169">Sets or returns the relative record number of a <strong>Recordset2</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-171"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-171"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-172">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-173">Renvoie le nombre d'enregistrements dont la dernière mise à jour par lot n'a pas pu se terminer (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-175"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-176">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-177">Renvoie un tableau de signets indiquant les lignes à l'origine de conflits dans la dernière opération de mise à jour par lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-179"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-179"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-180">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-181">Définit ou renvoie le nombre d'instructions renvoyées au serveur dans chaque lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-183">Renvoie une valeur qui indique si la position d'enregistrement actuelle précède le premier enregistrement d'un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="2317b-184">Type <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-186">Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif dans un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-188">Renvoie une valeur indiquant si un objet <strong>Recordset</strong> prend en charge les signets, que vous pouvez définir à l'aide de la propriété <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-190">Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="2317b-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="2317b-191">Valeur <strong>Long</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2317b-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-193">Définit ou renvoie une valeur spécifiant le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique qui contient des données d'une source de données ODBC à placer dans le cache local (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-195">Renvoie l'objet <strong><a href="connection-object-dao.md">Connection</a></strong> qui correspond à la base de données.</span><span class="sxs-lookup"><span data-stu-id="2317b-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-197">Renvoie la date et l'heure de création d'une table de base (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2317b-198">Type <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-200">Renvoie une valeur indiquant l'état de modification de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2317b-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-202">Renvoie une valeur qui indique si la position d'enregistrement actuelle suit le dernier enregistrement d'un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="2317b-203"><strong>Boolean</strong> (en lecture seule).</span><span class="sxs-lookup"><span data-stu-id="2317b-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-205">Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés pour l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="2317b-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="2317b-206">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-207"><strong><a href="recordset2-filter-property-dao.md">Filtre</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-208">Définit ou renvoie une valeur qui détermine les enregistrements inclus dans l'objet <strong>Recordset</strong> ouvert ultérieurement (espace de travail Microsoft Access uniquement.</span><span class="sxs-lookup"><span data-stu-id="2317b-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2317b-209">Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2317b-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-211">Définit ou renvoie une valeur qui indique le nom de l'objet <strong><a href="index-object-dao.md">Index</a></strong> actif dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-213">Renvoie un signet indiquant le dernier enregistrement ajouté ou modifié.</span><span class="sxs-lookup"><span data-stu-id="2317b-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-215">Renvoie la date et l'heure de la dernière modification apportée à une table de base.</span><span class="sxs-lookup"><span data-stu-id="2317b-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="2317b-216">Type <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-218">Définit ou renvoie une valeur indiquant le type de verrouillage appliqué pendant l'opération de modification.</span><span class="sxs-lookup"><span data-stu-id="2317b-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-220">Renvoie le nom de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="2317b-220">Returns the name of the specified object.</span></span> <span data-ttu-id="2317b-221">En lecture seule <strong>chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-223">Indique si un enregistrement donné a été localisé à l'aide de la méthode <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> ou de l'une des méthodes <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-223">Indicates whether a particular record was found by using the <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-225">Renvoie l'objet <strong>Recordset</strong> parent de l'objet Recordset défini.</span><span class="sxs-lookup"><span data-stu-id="2317b-225">Returns the parent <strong>Recordset</strong> of the specified recordset.</span></span> <span data-ttu-id="2317b-226">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-226">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-228">Définit ou renvoie une valeur indiquant l'emplacement approximatif de l'enregistrement actif dans l'objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en fonction du pourcentage d'enregistrements dans cet objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2317b-228">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-229"><strong><a href="recordset2-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-229"><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-230">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="2317b-230">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="2317b-231">Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-231">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-p120">Renvoie le nombre d'enregistrements accédés dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> ou le nombre total d'enregistrements dans un objet <strong>Recordset</strong> de type table ou un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. Type <strong>Long</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-p120">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-237"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-237"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-238">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-238">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-p122">Renvoie un valeur indiquant l'état de mise à jour de l'enregistrement actif s'il fait partie d'une mise à jour par lot (espaces de travail ODBCDirect uniquement). Type <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-p122">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-242">Renvoie une valeur indiquant si un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> prend en charge la méthode <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong>, laquelle réexécute la requête sur laquelle l'objet <strong>Recordset</strong> est basé.</span><span class="sxs-lookup"><span data-stu-id="2317b-242">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-244">Définit ou renvoie l'ordre de tri des enregistrements d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> (espace de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-244">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-246"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-246"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-247">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-247">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-248">Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <strong>dbRunAsync</strong>) est terminée (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2317b-248">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-250">Renvoie une valeur qui indique si un objet prend en charge les transactions.</span><span class="sxs-lookup"><span data-stu-id="2317b-250">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="2317b-251">Valeur <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-251">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-252"><strong><a href="recordset2-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-252"><strong><a href="recordset2-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-253">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="2317b-253">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="2317b-254">Type de données <strong>Integer</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-254">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-256">Renvoie une valeur qui indique si vous pouvez changer un objet DAO.</span><span class="sxs-lookup"><span data-stu-id="2317b-256">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="2317b-257">Type de données <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-257">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-259"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2317b-259"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2317b-260">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2317b-260">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2317b-p128">Définit ou renvoie une valeur qui indique la manière dont est construite la clause WHERE pour chaque enregistrement pendant une mise à jour par lot, et si cette dernière doit utiliser une instruction UPDATE ou DELETE suivie d'un INSERT (espaces de travail ODBCDirect uniquement). Type de données <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>. En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2317b-p128">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2317b-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-264">Définit ou renvoie une valeur qui valide les données dans un champ au moment de leur modification ou de leur ajout à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2317b-264">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2317b-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="2317b-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2317b-p129">Définit ou renvoie une valeur spécifiant le texte du message affiché par votre application si la valeur d'un objet <strong>Field</strong> ne respecte pas la règle de validation définie par le paramètre de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2317b-p129">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

