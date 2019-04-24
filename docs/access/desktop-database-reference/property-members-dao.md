---
title: Membres de propriété (DAO)
TOCTitle: Property Members
ms:assetid: 32658adb-f153-148d-a216-eb97b996579a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192303(v=office.15)
ms:contentKeyID: 48544076
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe60c12a85eff0dd8f796f9affeef71979dac580
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301210"
---
# <a name="property-members-dao"></a><span data-ttu-id="6f5c8-102">Membres de propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f5c8-102">Property members (DAO)</span></span>


<span data-ttu-id="6f5c8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f5c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f5c8-104">Un objet Property représente une caractéristique prédéfinie ou définie par l'utilisateur d'un objet DAO.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-104">A Property object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="properties"></a><span data-ttu-id="6f5c8-105">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f5c8-105">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f5c8-106">Nom</span><span class="sxs-lookup"><span data-stu-id="6f5c8-106">Name</span></span></p></th>
<th><p><span data-ttu-id="6f5c8-107">Description</span><span class="sxs-lookup"><span data-stu-id="6f5c8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f5c8-108"><strong><a href="property-inherited-property-dao.md">Héritées</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f5c8-108"><strong><a href="property-inherited-property-dao.md">Inherited</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f5c8-109">Renvoie une valeur qui indique si un objet <strong><a href="property-object-dao.md">Property</a></strong> est hérité d'un objet sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-109">Returns a value that indicates whether a <strong><a href="property-object-dao.md">Property</a></strong> object is inherited from an underlying object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5c8-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f5c8-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f5c8-p101">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-p101">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5c8-114"><strong><a href="property-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f5c8-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f5c8-115">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-115">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="6f5c8-116">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-116">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5c8-117"><strong><a href="property-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f5c8-117"><strong><a href="property-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f5c8-118">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-118">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="6f5c8-119">Type de données <strong>Integer</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-119">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5c8-120"><strong><a href="property-value-property-dao.md">Valeur</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f5c8-120"><strong><a href="property-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f5c8-121">Définit ou renvoie la valeur d'un objet.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-121">Sets or returns the value of an object.</span></span> <span data-ttu-id="6f5c8-122">Type de données <strong>Variant</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="6f5c8-122">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

