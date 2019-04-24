---
title: Membres du document (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd50ec72113b0615849ff6b8b2e8d73c0e61c3ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293790"
---
# <a name="document-members-dao"></a><span data-ttu-id="867d3-102">Membres du document (DAO)</span><span class="sxs-lookup"><span data-stu-id="867d3-102">Document members (DAO)</span></span>


<span data-ttu-id="867d3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="867d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="867d3-p101">Un objet Document inclut des informations sur une instance d'un objet. L'objet peut être une base de données, une table enregistrée, une requête ou une relation (bases de données de moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="867d3-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="867d3-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="867d3-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="867d3-107">Nom</span><span class="sxs-lookup"><span data-stu-id="867d3-107">Name</span></span></p></th>
<th><p><span data-ttu-id="867d3-108">Description</span><span class="sxs-lookup"><span data-stu-id="867d3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="867d3-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="867d3-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="867d3-110">Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="867d3-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="867d3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="867d3-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="867d3-112">Nom</span><span class="sxs-lookup"><span data-stu-id="867d3-112">Name</span></span></p></th>
<th><p><span data-ttu-id="867d3-113">Description</span><span class="sxs-lookup"><span data-stu-id="867d3-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="867d3-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span><span class="sxs-lookup"><span data-stu-id="867d3-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="867d3-115">Renvoie le nom de l'objet <strong><a href="container-object-dao.md">Container</a></strong> auquel appartient un objet <strong>document</strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="867d3-115">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="867d3-116">.</span><span class="sxs-lookup"><span data-stu-id="867d3-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="867d3-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="867d3-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="867d3-118">Renvoie la date et l'heure de création d'un objet.</span><span class="sxs-lookup"><span data-stu-id="867d3-118">Returns the date and time that an object was created.</span></span> <span data-ttu-id="867d3-119">Valeur de type <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="867d3-119">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="867d3-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="867d3-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="867d3-121">Renvoie la date et l'heure de la dernière modification apportée à un objet.</span><span class="sxs-lookup"><span data-stu-id="867d3-121">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="867d3-122">Type de données <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="867d3-122">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="867d3-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="867d3-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="867d3-124">Renvoie le nom de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="867d3-124">Returns the name of the specified object.</span></span> <span data-ttu-id="867d3-125">En lecture seule <strong>chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="867d3-125">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="867d3-126"><strong><a href="document-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="867d3-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="867d3-127">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="867d3-127">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="867d3-128">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="867d3-128">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

