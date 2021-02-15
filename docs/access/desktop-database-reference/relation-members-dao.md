---
title: Relation members (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84e18afe4a11e53d68397efad71ac6136c779143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307036"
---
# <a name="relation-members-dao"></a><span data-ttu-id="67557-102">Relation members (DAO)</span><span class="sxs-lookup"><span data-stu-id="67557-102">Relation members (DAO)</span></span>


<span data-ttu-id="67557-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67557-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67557-104">Un objet Relation représente une relation entre des champs de tables ou de requêtes (bases de données de moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="67557-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="67557-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67557-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67557-106">Nom</span><span class="sxs-lookup"><span data-stu-id="67557-106">Name</span></span></p></th>
<th><p><span data-ttu-id="67557-107">Description</span><span class="sxs-lookup"><span data-stu-id="67557-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67557-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-109">Crée un objet <strong><a href="field-object-dao.md">Field</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="67557-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="67557-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67557-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67557-111">Nom</span><span class="sxs-lookup"><span data-stu-id="67557-111">Name</span></span></p></th>
<th><p><span data-ttu-id="67557-112">Description</span><span class="sxs-lookup"><span data-stu-id="67557-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67557-113"><strong><a href="relation-attributes-property-dao.md">Attributs</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-114">Définit ou renvoie une valeur spécifiant une ou plusieurs caractéristiques d'un objet <strong>Relation</strong>.</span><span class="sxs-lookup"><span data-stu-id="67557-114">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object.</span></span> <span data-ttu-id="67557-115">Type <strong>Long</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="67557-115">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67557-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-117">Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés pour l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="67557-117">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="67557-118">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="67557-118">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67557-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-120">Définit ou renvoie le nom de la table étrangère dans une relation (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="67557-120">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="67557-121">.</span><span class="sxs-lookup"><span data-stu-id="67557-121">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67557-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-p104">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="67557-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67557-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-p105">Définit ou renvoie une valeur sur une <strong>Relation</strong> indiquant si cette relation doit être prise en compte lors du remplissage d'un réplica partiel à partir d'un réplica complet. (Bases de données de moteur de base de données Microsoft Access uniquement). Type de données <strong>Boolean</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="67557-p105">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67557-130"><strong><a href="relation-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-131">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="67557-131">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="67557-132">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="67557-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67557-133"><strong><a href="relation-table-property-dao.md">Tableau</a></strong></span><span class="sxs-lookup"><span data-stu-id="67557-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="67557-p107">Indique le nom d'une table primaire d'un objet <strong><a href="relation-object-dao.md">Relation</a></strong>. Ce nom doit correspondre à la valeur de la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> d'un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong> ou <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="67557-p107">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table. This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

