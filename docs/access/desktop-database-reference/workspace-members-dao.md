---
title: Membres de l’espace de travail (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 525b261f5184f520d6f24c81f3d446fee8aa800e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936958"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="6c1cb-102">Membres de l’espace de travail (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c1cb-102">Workspace members (DAO)</span></span>


<span data-ttu-id="6c1cb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c1cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c1cb-p101">Un objet Workspace définit une session nommée pour un utilisateur. Il contient des bases de données ouvertes et fournit les mécanismes destinés aux transactions simultanées, ainsi que la prise en charge des groupes de travail sécurisés dans les espaces de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p101">A Workspace object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="6c1cb-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6c1cb-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1cb-107">Nom</span><span class="sxs-lookup"><span data-stu-id="6c1cb-107">Name</span></span></p></th>
<th><p><span data-ttu-id="6c1cb-108">Description</span><span class="sxs-lookup"><span data-stu-id="6c1cb-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-p102">Commence une nouvelle transaction. <strong>Database</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p102">Begins a new transaction. Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-113">Ferme un objet <strong>Workspace</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-115">Met fin à la transaction en cours et enregistre les modifications.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-117">Crée un objet <strong><a href="database-object-dao.md">Database</a></strong>, enregistre la base de données sur le disque, et renvoie un objet <strong>Database</strong> ouvert (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="6c1cb-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-118"><strong><a href="workspace-openconnection-method-dao.md">Méthode OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-119"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-119"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6c1cb-120">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="6c1cb-121">Ouvre un objet <strong><a href="connection-object-dao.md">Connection</a></strong> dans une source de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="6c1cb-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-123">Ouvre une base de données spécifiée dans un objet <strong><a href="workspace-object-dao.md">Workspace</a></strong> et renvoie une référence à l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui le représente.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-125">Met fin à transaction en cours et restaure les bases de données dans l'objet <strong>Workspace</strong> à l'état dans lequel elles se trouvaient au début de la transaction actuelle.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="6c1cb-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c1cb-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1cb-127">Nom</span><span class="sxs-lookup"><span data-stu-id="6c1cb-127">Name</span></span></p></th>
<th><p><span data-ttu-id="6c1cb-128">Description</span><span class="sxs-lookup"><span data-stu-id="6c1cb-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-p104">Renvoie une collection <strong>Connections</strong> qui représente les connexions actives dans l'objet <strong>Workspace</strong> spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p104">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-p105">Renvoie une collection <strong>Databases</strong> qui représente les bases de données ouvertes dans l'objet <strong>Workspace</strong> spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p105">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-136"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-136"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6c1cb-137">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-137">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="6c1cb-138">Définit ou renvoie le type de pilote de curseur utilisé pour la connexion créée par la méthode <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> ou <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="6c1cb-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-140">Définit ou renvoie une valeur qui indique si plusieurs transactions impliquant la même source de données ODBC connectée au moteur de base de données Microsoft Access sont isolées (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="6c1cb-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-142">Définit ou renvoie le nombre de secondes devant s'écouler avant l'apparition d'une erreur lorsque vous essayez de vous connecter à une base de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-p107">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1cb-147"><strong><a href="workspace-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-p108">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p108">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1cb-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c1cb-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c1cb-p109">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données <strong>Integer</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6c1cb-p109">Sets or returns a value that indicates the operational type or data type of an object. Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

