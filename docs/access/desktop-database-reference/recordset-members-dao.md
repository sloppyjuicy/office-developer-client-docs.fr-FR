---
title: Membres de l’objet Recordset (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73c83f4bba44ed7e30a45a02b1b273beb85a2851
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928291"
---
# <a name="recordset-members-dao"></a><span data-ttu-id="3577c-102">Membres de l’objet Recordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="3577c-102">Recordset members (DAO)</span></span>


<span data-ttu-id="3577c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3577c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3577c-104">Un objet Recordset représente les enregistrements dans une table de base ou les enregistrements obtenus par l'exécution d'une requête.</span><span class="sxs-lookup"><span data-stu-id="3577c-104">A Recordset object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="3577c-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3577c-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3577c-106">Nom</span><span class="sxs-lookup"><span data-stu-id="3577c-106">Name</span></span></p></th>
<th><p><span data-ttu-id="3577c-107">Description</span><span class="sxs-lookup"><span data-stu-id="3577c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3577c-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-109">Crée un nouvel enregistrement pour un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualisable.</span><span class="sxs-lookup"><span data-stu-id="3577c-109">Creates a new record for an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-110"><strong><a href="recordset-cancel-method-dao.md">Annuler</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p101">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-113">Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-115">Annule toutes les mises à jour en attente d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-117">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> dupliqué qui fait référence à l'objet <strong>Recordset</strong> d'origine.</span><span class="sxs-lookup"><span data-stu-id="3577c-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-119">Ferme un objet <strong>Recordset</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="3577c-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-121">Renvoie un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong> qui est une copie de l' <strong>objet QueryDef</strong> utilisé pour créer l’objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> représenté par l’espace réservé du jeu d’enregistrements (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3577c-122">.</span><span class="sxs-lookup"><span data-stu-id="3577c-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-124">Méthode non prise en charge pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="3577c-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-126">Copie l'enregistrement actif d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> modifiable vers la mémoire tampon de copie pour modification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3577c-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-128">Remplit une partie ou l'ensemble d'un cache local pour un objet <strong>Recordset</strong> qui contient des données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-130">Localise le premier enregistrement dans un objet <strong>Recordset</strong> de type feuille de réponse dynamique ou capture instantanée qui remplit les critères spécifiés et rend l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-132">Recherche le dernier enregistrement dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p103">Recherche l'enregistrement suivant dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p104">Recherche l'enregistrement précédent dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-140">Récupère plusieurs lignes d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-141"><strong><a href="recordset-move-method-dao.md">Déplacer</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-142">Déplace l'enregistrement actif d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-144">Atteint le premier enregistrement d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="3577c-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-146">Atteint le dernier enregistrement d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="3577c-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-148">Se déplace jusqu'à l'enregistrement suivant dans un objet <strong>Recordset</strong> spécifié et définit cet enregistrement comme l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="3577c-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-150">Atteint l'enregistrement précédent d'un objet <strong>Recordset</strong> spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="3577c-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p105">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p105">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-154">Obtient le jeu d'enregistrements suivant, le cas échéant, qui est renvoyé par une requête Sélection à parties multiples dans le cadre d'un appel <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong>, et renvoie une valeur de type <strong>Boolean</strong> indiquant si un ou plusieurs enregistrements supplémentaires sont en attente (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-156">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-157"><strong><a href="recordset-requery-method-dao.md">Actualiser</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-158">Met à jour les données d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="3577c-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-160">Localise l'enregistrement dans un objet <strong>Recordset</strong> de type table indexée en fonction des critères spécifiés pour l'index actuel et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p106">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-164">Enregistre le contenu de la mémoire tampon de la copie dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> modifiable.</span><span class="sxs-lookup"><span data-stu-id="3577c-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="3577c-165">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3577c-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3577c-166">Nom</span><span class="sxs-lookup"><span data-stu-id="3577c-166">Name</span></span></p></th>
<th><p><span data-ttu-id="3577c-167">Description</span><span class="sxs-lookup"><span data-stu-id="3577c-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3577c-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-169">Définit ou renvoie le numéro d’enregistrement relatif de l’enregistrement actif d’un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-169">Sets or returns the relative record number of a <strong>Recordset</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p107">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p107">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-173">Renvoie le nombre d'enregistrements dont la dernière mise à jour par lot n'a pas été exécutée (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p108">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-177">Renvoie un tableau de signets indiquant les lignes qui ont généré des collisions lors de la dernière mise à jour par lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p109">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p109">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-181">Définit ou renvoie le nombre d'instructions renvoyées au serveur dans chaque lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p110">Renvoie une valeur qui indique si la position de l'enregistrement actif est située avant le premier enregistrement dans un objet <strong>Recordset</strong>. Valeur de type <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p110">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-185"><strong><a href="recordset-bookmark-property-dao.md">Signet</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-186">Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-188">Renvoie une valeur qui indique si un objet <strong>Recordset</strong> prend en charge les signets, que vous pouvez définir à l'aide de la propriété <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p111">Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur <strong>Long</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="3577c-p111">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-193">Définit ou renvoie une valeur qui spécifie le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique contenant des données à mettre en cache local à partir d'une source de données ODBC (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-195">Renvoie l'objet <strong><a href="connection-object-dao.md">Connection</a></strong> qui correspond à la base de données.</span><span class="sxs-lookup"><span data-stu-id="3577c-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p112">Renvoie la date et l'heure de création d'une table de base (espaces de travail Microsoft Access uniquement). Valeur <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p112">Returns the date and time a base table was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-200">Renvoie une valeur qui indique l'état de modification de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="3577c-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p113">Renvoie une valeur qui indique si la position d'enregistrement actuelle suit le dernier enregistrement d'un objet <strong>Recordset</strong>. Type <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p113">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-204"><strong><a href="recordset-fields-property-dao.md">Champs</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p114">Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés pour l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p114">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p115">Définit ou renvoie une valeur qui détermine les enregistrements inclus dans un objet <strong>Recordset</strong> ouvert par la suite (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="3577c-p115">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-211">Définit ou renvoie une valeur qui indique le nom de l'objet <strong><a href="index-object-dao.md">Index</a></strong> actif d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-213">Renvoie un signet indiquant le dernier enregistrement ajouté ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3577c-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p116">Renvoie la date et l'heure de la dernière modification apportée à une table de base. Type <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p116">Returns the date and time of the most recent change made to a base table. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-218">Définit ou renvoie une valeur indiquant le type de verrouillage utilisé lors de l'édition.</span><span class="sxs-lookup"><span data-stu-id="3577c-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p117">Renvoie le nom de l'objet spécifié. Type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p117">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-223">Indique si un enregistrement donné a été localisé à l'aide de la méthode <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> ou de l'une des méthodes <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-223">Indicates whether a particular record was found by using the <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-225">Définit ou renvoie une valeur indiquant l'emplacement approximatif de l'enregistrement actif dans l'objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en fonction du pourcentage d'enregistrements dans cet objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="3577c-225">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-226"><strong><a href="recordset-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p118">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p118">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p119">Renvoie le nombre d'enregistrements accédés dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> ou le nombre total d'enregistrements dans un objet <strong>Recordset</strong> de type table ou un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. Type <strong>Long</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p119">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p120">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p120">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-p121">Renvoie un valeur indiquant l'état de mise à jour de l'enregistrement actif s'il fait partie d'une mise à jour par lot (espaces de travail ODBCDirect uniquement). Type <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p121">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-239">Renvoie une valeur indiquant si un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> prend en charge la méthode <strong><a href="recordset-requery-method-dao.md">Requery</a></strong>, laquelle réexécute la requête sur laquelle l'objet <strong>Recordset</strong> est basé.</span><span class="sxs-lookup"><span data-stu-id="3577c-239">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-241">Définit ou renvoie l'ordre de tri des enregistrements d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> (espace de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-241">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p122">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p122">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-245">Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <strong>dbRunAsync</strong>) est terminée (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="3577c-245">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p123">Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p123">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-249"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="3577c-249"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-250">La description de ce membre apparaîtra dans la version finale d'Office 14.</span><span class="sxs-lookup"><span data-stu-id="3577c-250">The description for this member will appear in the final release of Office 14.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p124">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p124">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions (OptionsMAJ)</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="3577c-p125">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3577c-p125">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="3577c-p126">Définit ou renvoie une valeur qui indique la manière dont est construite la clause WHERE pour chaque enregistrement pendant une mise à jour par lot, et si cette dernière doit utiliser une instruction UPDATE ou DELETE suivie d'un INSERT (espaces de travail ODBCDirect uniquement). Type de données <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>. En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3577c-p126">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3577c-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-260">Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="3577c-260">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3577c-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="3577c-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3577c-p127">Définit ou renvoie une valeur spécifiant le texte du message affiché par votre application si la valeur d'un objet <strong>Field</strong> ne respecte pas la règle de validation définie par le paramètre de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3577c-p127">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

