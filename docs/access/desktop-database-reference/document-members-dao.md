---
title: Document Members (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ae19e30aa2a2f60f606f2380712815732eac932
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871366"
---
# <a name="document-members-dao"></a><span data-ttu-id="cda94-102">Document Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="cda94-102">Document Members (DAO)</span></span>


<span data-ttu-id="cda94-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cda94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cda94-p101">Un objet Document inclut des informations sur une instance d'un objet. L'objet peut être une base de données, une table enregistrée, une requête ou une relation (bases de données de moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="cda94-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="cda94-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cda94-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cda94-107">Nom</span><span class="sxs-lookup"><span data-stu-id="cda94-107">Name</span></span></p></th>
<th><p><span data-ttu-id="cda94-108">Description</span><span class="sxs-lookup"><span data-stu-id="cda94-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cda94-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="cda94-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cda94-110">Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="cda94-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="cda94-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cda94-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cda94-112">Nom</span><span class="sxs-lookup"><span data-stu-id="cda94-112">Name</span></span></p></th>
<th><p><span data-ttu-id="cda94-113">Description</span><span class="sxs-lookup"><span data-stu-id="cda94-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cda94-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span><span class="sxs-lookup"><span data-stu-id="cda94-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cda94-p102">Renvoie le nom de l'objet <strong><a href="container-object-dao.md">Container</a></strong> auquel un objet <strong>Document</strong> appartient (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="cda94-p102">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cda94-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="cda94-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cda94-p103">Renvoie la date et l'heure de création d'un objet. Valeur de type <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cda94-p103">Returns the date and time that an object was created. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cda94-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="cda94-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cda94-p104">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données <strong>Variant</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cda94-p104">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cda94-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="cda94-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cda94-p105">Renvoie le nom de l'objet spécifié. Type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cda94-p105">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cda94-126"><strong><a href="document-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="cda94-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cda94-p106">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cda94-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

