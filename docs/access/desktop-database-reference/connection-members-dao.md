---
title: Connection Members (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 098f44d87390351c23e61000ecbe47eae35810ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295904"
---
# <a name="connection-members-dao"></a><span data-ttu-id="c20f7-102">Connection Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="c20f7-102">Connection members (DAO)</span></span>

<span data-ttu-id="c20f7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c20f7-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="c20f7-104">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="c20f7-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c20f7-105">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c20f7-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="c20f7-106">Un objet Connection représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="c20f7-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 
## <a name="methods"></a><span data-ttu-id="c20f7-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c20f7-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c20f7-108">Nom</span><span class="sxs-lookup"><span data-stu-id="c20f7-108">Name</span></span></p></th>
<th><p><span data-ttu-id="c20f7-109">Description</span><span class="sxs-lookup"><span data-stu-id="c20f7-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-110"><strong><a href="connection-cancel-method-dao.md">Annuler</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-111">Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="c20f7-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-113">Ferme un objet <strong>Connection</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="c20f7-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-115">Crée un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="c20f7-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-117">Exécute une requête action ou exécute une instruction SQL sur l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="c20f7-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-119">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l’ajoute à la collection <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="c20f7-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="c20f7-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c20f7-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c20f7-121">Nom</span><span class="sxs-lookup"><span data-stu-id="c20f7-121">Name</span></span></p></th>
<th><p><span data-ttu-id="c20f7-122">Description</span><span class="sxs-lookup"><span data-stu-id="c20f7-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-124">Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte.</span><span class="sxs-lookup"><span data-stu-id="c20f7-124">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="c20f7-125">Valeur de type <strong>String</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c20f7-125">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-127">Renvoie l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui correspond à cette connexion (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="c20f7-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-129">Renvoie le nom d'un objet <strong><a href="connection-object-dao.md">Connection</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="c20f7-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-131">Renvoie une collection <strong>QueryDefs</strong> qui contient tous les objets <strong>QueryDef</strong> de la connexion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c20f7-131">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection.</span></span> <span data-ttu-id="c20f7-132">Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c20f7-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-134">Définit ou renvoie une valeur qui spécifie la durée d'attente (en secondes) avant qu'une erreur d'expiration ne se produise lors de l'exécution d'une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="c20f7-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-136">Renvoie le nombre d'enregistrements affectés par le dernier appel de la méthode <strong><a href="connection-execute-method-dao.md">Execute</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="c20f7-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-138">Renvoie une collection <strong>Recordsets</strong> qui contient tous les jeux d'enregistrements ouverts pour la connexion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c20f7-138">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection.</span></span> <span data-ttu-id="c20f7-139">Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c20f7-139">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-141">Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <strong>dbRunAsync</strong>) est terminée (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="c20f7-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c20f7-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-143">Renvoie une valeur qui indique si un objet prend en charge les transactions.</span><span class="sxs-lookup"><span data-stu-id="c20f7-143">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="c20f7-144"><strong>Boolean</strong> (en lecture seule).</span><span class="sxs-lookup"><span data-stu-id="c20f7-144">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c20f7-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="c20f7-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c20f7-146">Renvoie une valeur qui indique si vous pouvez changer un objet DAO.</span><span class="sxs-lookup"><span data-stu-id="c20f7-146">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="c20f7-147">Type de données <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c20f7-147">Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

