---
title: Membres de l’index (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709158"
---
# <a name="index-members-dao"></a><span data-ttu-id="ea6e8-102">Membres de l’index (DAO)</span><span class="sxs-lookup"><span data-stu-id="ea6e8-102">Index members (DAO)</span></span>


<span data-ttu-id="ea6e8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea6e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea6e8-p101">Les objets Index déterminent l'ordre des enregistrements accessibles depuis les tables de base de données et indiquent si les enregistrements en double sont acceptés ou pas, ce qui optimise l'accès aux données. Dans le cas d'une base de données externe, les objets Index décrivent les index définis pour les tables externes (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-p101">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="ea6e8-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea6e8-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea6e8-107">Nom</span><span class="sxs-lookup"><span data-stu-id="ea6e8-107">Name</span></span></p></th>
<th><p><span data-ttu-id="ea6e8-108">Description</span><span class="sxs-lookup"><span data-stu-id="ea6e8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea6e8-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-110">Crée un objet <strong><a href="field-object-dao.md">Field</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea6e8-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-112">Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="ea6e8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea6e8-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea6e8-114">Nom</span><span class="sxs-lookup"><span data-stu-id="ea6e8-114">Name</span></span></p></th>
<th><p><span data-ttu-id="ea6e8-115">Description</span><span class="sxs-lookup"><span data-stu-id="ea6e8-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea6e8-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-p102">Définit ou renvoie une valeur qui indique si un objet <strong>Index</strong> représente un index cluster pour une table (espaces de travail Microsoft Access uniquement). Valeur de type <strong>Boolean</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ea6e8-p102">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea6e8-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-120">Renvoie une valeur indiquant le nombre de valeurs uniques pour l'objet <strong><a href="index-object-dao.md">Index</a></strong> inclus dans la table associée (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea6e8-121"><strong><a href="index-fields-property-dao.md">Champs</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-p103">Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés de l'objet spécifié. Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ea6e8-p103">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea6e8-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-p104">Renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente une clé étrangère d'une table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-p104">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea6e8-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-128">Définit ou renvoie une valeur qui indique si les enregistrements ayant des valeurs nulles dans leurs champs d'index ont des entrées d'index (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea6e8-129"><strong><a href="index-name-property-dao.md">Nom</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-p105">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="ea6e8-p105">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea6e8-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-134">Définit ou renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente un index de clé primaire pour une table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea6e8-135"><strong><a href="index-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-p106">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ea6e8-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea6e8-138"><strong><a href="index-required-property-dao.md">Obligatoire</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-139">Définit ou renvoie une valeur qui indique si un objet <strong><a href="field-object-dao.md">Field</a></strong> requiert une valeur non Null.</span><span class="sxs-lookup"><span data-stu-id="ea6e8-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea6e8-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span><span class="sxs-lookup"><span data-stu-id="ea6e8-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="ea6e8-141">Définit ou renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente un index (une clé) unique d'une table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea6e8-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

