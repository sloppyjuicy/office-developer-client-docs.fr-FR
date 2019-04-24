---
title: Workspace, membres (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a2105c13f5f7ce9a75e7e18e20477d8b283543a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302591"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="a3b54-102">Workspace, membres (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3b54-102">Workspace members (DAO)</span></span>


<span data-ttu-id="a3b54-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3b54-p101">Un objet Workspace définit une session nommée pour un utilisateur. Il contient des bases de données ouvertes et fournit les mécanismes destinés aux transactions simultanées, ainsi que la prise en charge des groupes de travail sécurisés dans les espaces de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a3b54-p101">A Workspace object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="a3b54-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3b54-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3b54-107">Nom</span><span class="sxs-lookup"><span data-stu-id="a3b54-107">Name</span></span></p></th>
<th><p><span data-ttu-id="a3b54-108">Description</span><span class="sxs-lookup"><span data-stu-id="a3b54-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-110">Commence une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="a3b54-110">Begins a new transaction.</span></span> <span data-ttu-id="a3b54-111"><strong>Database</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a3b54-111">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-113">Ferme un objet <strong>Workspace</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="a3b54-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-115">Met fin à la transaction en cours et enregistre les modifications.</span><span class="sxs-lookup"><span data-stu-id="a3b54-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-116"><strong><a href="workspace-createdatabase-method-dao.md">Database</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-117">Crée un objet <strong><a href="database-object-dao.md">Database</a></strong>, enregistre la base de données sur le disque, et renvoie un objet <strong>Database</strong> ouvert (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a3b54-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-119"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="a3b54-119"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="a3b54-120">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a3b54-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="a3b54-121">Ouvre un objet <strong><a href="connection-object-dao.md">Connection</a></strong> dans une source de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="a3b54-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-123">Ouvre une base de données spécifiée dans un objet <strong><a href="workspace-object-dao.md">Workspace</a></strong> et renvoie une référence à l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui le représente.</span><span class="sxs-lookup"><span data-stu-id="a3b54-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-125">Met fin à transaction en cours et restaure les bases de données dans l'objet <strong>Workspace</strong> à l'état dans lequel elles se trouvaient au début de la transaction actuelle.</span><span class="sxs-lookup"><span data-stu-id="a3b54-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="a3b54-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a3b54-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3b54-127">Nom</span><span class="sxs-lookup"><span data-stu-id="a3b54-127">Name</span></span></p></th>
<th><p><span data-ttu-id="a3b54-128">Description</span><span class="sxs-lookup"><span data-stu-id="a3b54-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-130">Renvoie une collection <strong>Connections</strong> qui représente les connexions actives dans l'objet <strong>Workspace</strong> spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3b54-130">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="a3b54-131">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a3b54-131">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-133">Renvoie une collection <strong>Databases</strong> qui représente les bases de données ouvertes dans l'objet <strong>Workspace</strong> spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3b54-133">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="a3b54-134">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a3b54-134">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-136"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="a3b54-136"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="a3b54-137">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a3b54-137">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="a3b54-138">Définit ou renvoie le type de pilote de curseur utilisé pour la connexion créée par la méthode <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> ou <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="a3b54-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans,</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-140">Définit ou renvoie une valeur qui indique si plusieurs transactions impliquant la même source de données ODBC connectée au moteur de base de données Microsoft Access sont isolées (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a3b54-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-142">Définit ou renvoie le nombre de secondes devant s'écouler avant l'apparition d'une erreur lorsque vous essayez de vous connecter à une base de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="a3b54-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-p107">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="a3b54-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3b54-147"><strong><a href="workspace-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-148">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3b54-148">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="a3b54-149">Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a3b54-149">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3b54-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="a3b54-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a3b54-151">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="a3b54-151">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="a3b54-152">Type de données <strong>Integer</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a3b54-152">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

