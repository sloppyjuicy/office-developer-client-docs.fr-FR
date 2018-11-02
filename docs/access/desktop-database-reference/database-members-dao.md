---
title: Membres de base de données (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b75fff8251e74a525798cd5eb2c6feb2d69016b7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919751"
---
# <a name="database-members-dao"></a><span data-ttu-id="7ca3d-102">Membres de base de données (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ca3d-102">Database members (DAO)</span></span>


<span data-ttu-id="7ca3d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ca3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ca3d-104">Un objet Database représente une base de données ouverte.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-104">A Database object represents an open database.</span></span>

## <a name="methods"></a><span data-ttu-id="7ca3d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7ca3d-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ca3d-106">Nom</span><span class="sxs-lookup"><span data-stu-id="7ca3d-106">Name</span></span></p></th>
<th><p><span data-ttu-id="7ca3d-107">Description</span><span class="sxs-lookup"><span data-stu-id="7ca3d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-108"><strong><a href="database-close-method-dao.md">Fermer</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-108"><strong><a href="database-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-109">Ferme un objet <strong>Database</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-109">Closes an open <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-110"><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-110"><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p101">Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p101">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-113"><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-113"><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-114">Crée un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-114">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-115"><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-115"><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p102">Crée un nouvel objet <strong><a href="relation-object-dao.md">Relation</a></strong> (Espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p102">Creates a new <strong><a href="relation-object-dao.md">Relation</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-118"><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-118"><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p103">Crée un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p103">Creates a new <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-121"><strong><a href="database-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-121"><strong><a href="database-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-122">Exécute une requête Action ou une instruction SQL sur l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-122">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-123"><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-123"><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-124">Crée un nouveau réplica à partir d'un autre réplica de base de données (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-124">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-125"><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-125"><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-126">Permet de modifier le mot de passe d'une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-126">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-127"><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-127"><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-128">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-128">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-129"><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-129"><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p104">Synchronise les modifications d'un réplica partiel avec le réplica complet, efface tous les enregistrements du réplica partiel, puis remplit à nouveau ce dernier en fonction des filtres de réplica actifs. (Bases de données du moteur de base de données Microsoft Access uniquement.)</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p104">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-132"><strong><a href="database-synchronize-method-dao.md">Synchroniser</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-132"><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p105">Synchronise deux réplicas. (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p105">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="7ca3d-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ca3d-135">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ca3d-136">Nom</span><span class="sxs-lookup"><span data-stu-id="7ca3d-136">Name</span></span></p></th>
<th><p><span data-ttu-id="7ca3d-137">Description</span><span class="sxs-lookup"><span data-stu-id="7ca3d-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-138"><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-138"><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p106">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur <strong>Long</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p106">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-141"><strong><a href="database-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-141"><strong><a href="database-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p107">Définit ou renvoie une valeur qui fournit des informations sur la source d'une base de données ouverte. Valeur de type <strong>String</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p107">Sets or returns a value that provides information about the source an open database. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-144"><strong><a href="database-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-144"><strong><a href="database-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="7ca3d-p108">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="7ca3d-147">Renvoie l'objet <strong><a href="connection-object-dao.md">Connection</a></strong> qui correspond à la base de données (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-147">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-148"><strong><a href="database-containers-property-dao.md">Containers</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-148"><strong><a href="database-containers-property-dao.md">Containers</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p109">Renvoie une collection <strong>Containers</strong> qui représente tous les objets <strong>Container</strong> de la base de données spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p109">Returns a <strong>Containers</strong> collection that represents all of the <strong>Container</strong> objects in the specifed database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-151"><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-151"><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-152">Définit ou renvoie une valeur de 16 octets qui identifie de façon unique le réplica-maître d'un jeu de réplicas (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-152">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-153"><strong><a href="database-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-153"><strong><a href="database-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p110">Renvoie le nom de l'objet spécifié. Type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p110">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-156"><strong><a href="database-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-156"><strong><a href="database-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p111">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-159"><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-159"><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p112">Renvoie une collection <strong>QueryDefs</strong> qui contient tous les objets <strong>QueryDef</strong> de la base de données spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p112">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-162"><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-162"><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-163">Définit ou retourne une valeur qui spécifie le nombre de secondes d'attente avant qu'une erreur de délai d'attente soit générée lors de l'exécution d'une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-163">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-164"><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-164"><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-165">Renvoie le nombre d'enregistrements affectés par le dernier appel de la méthode <strong><a href="connection-execute-method-dao.md">Execute</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-165">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-166"><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-166"><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p113">Renvoie une collection <strong>Recordsets</strong> qui contient tous les jeux d'enregistrements ouverts pour la base de données spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p113">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-169"><strong><a href="database-relations-property-dao.md">Relations</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-169"><strong><a href="database-relations-property-dao.md">Relations</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p114">Renvoie une collection <strong>Relations</strong> qui contient tous les objets <strong>Relation</strong> enregistrés pour la base de données spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p114">Returns a <strong>Relations</strong> collection that contains all of the stored <strong>Relation</strong> objects for the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-172"><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-172"><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-173">Renvoie une valeur de 16 octets qui identifie de façon unique un réplica de base de données (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7ca3d-173">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-174"><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-174"><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p115">Renvoie une collection <strong>TableDefs</strong> qui contient tous les objets <strong>TableDef</strong> enregistrés dans la base de données spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p115">Returns a <strong>TableDefs</strong> collection that contains all of the <strong>TableDef</strong> objects stored in the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-177"><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-177"><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p116">Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p116">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ca3d-180"><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-180"><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p117">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p117">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ca3d-183"><strong><a href="database-version-property-dao.md">Version</a></strong></span><span class="sxs-lookup"><span data-stu-id="7ca3d-183"><strong><a href="database-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7ca3d-p118">Dans un espace de travail Microsoft Access, renvoie la version du moteur de base de données Microsoft Jet ou Microsoft Access qui a créé la base de données. Valeur <strong>String</strong> en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ca3d-p118">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

