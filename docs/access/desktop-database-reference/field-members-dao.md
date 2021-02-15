---
title: Field members (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a0e448662384572163fca074e554a5e30be30a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293090"
---
# <a name="field-members-dao"></a><span data-ttu-id="e31fa-102">Field members (DAO)</span><span class="sxs-lookup"><span data-stu-id="e31fa-102">Field members (DAO)</span></span>


<span data-ttu-id="e31fa-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e31fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e31fa-104">Un objet Field représente une colonne de données avec un type de données communes et un ensemble commun de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e31fa-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="e31fa-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e31fa-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e31fa-106">Nom</span><span class="sxs-lookup"><span data-stu-id="e31fa-106">Name</span></span></p></th>
<th><p><span data-ttu-id="e31fa-107">Description</span><span class="sxs-lookup"><span data-stu-id="e31fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-109">Ajoute des données issues d'une expression de chaîne à un objet <strong><a href="field-object-dao.md">Field</a></strong> de type mémo ou binaire long dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="e31fa-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-111">Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="e31fa-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-113">Renvoie l’ensemble ou une partie du contenu d’un objet <strong>Memo</strong> ou <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> dans la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d’un <strong><a href="recordset-object-dao.md">objet Recordset.</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="e31fa-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e31fa-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e31fa-115">Nom</span><span class="sxs-lookup"><span data-stu-id="e31fa-115">Name</span></span></p></th>
<th><p><span data-ttu-id="e31fa-116">Description</span><span class="sxs-lookup"><span data-stu-id="e31fa-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-118">Définit ou renvoie une valeur qui indique si une chaîne de longueur nulle () est un paramètre valide pour la propriété Value de l’objet Field avec un type de données Texte ou Mémo (espaces de travail &quot; &quot; Microsoft Access uniquement). <strong><a href="field-value-property-dao.md"></a></strong> <strong><a href="field-object-dao.md"></a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-119"><strong><a href="field-attributes-property-dao.md">Attributs</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-120">Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet <strong><a href="field-object-dao.md">Field</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="e31fa-120">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object.</span></span> <span data-ttu-id="e31fa-121"><strong>Long</strong> (en lecture/écriture).</span><span class="sxs-lookup"><span data-stu-id="e31fa-121">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p102">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur <strong>Long</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e31fa-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-126">Renvoie une valeur qui indique si les données du champ représenté par un objet <strong><a href="field-object-dao.md">Field</a></strong> peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="e31fa-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p103">Définit ou renvoie la valeur par défaut d'un objet <strong><a href="field-object-dao.md">Field</a></strong>. Cette propriété est en lecture-écriture si l'objet <strong>Field</strong> n'est pas encore ajouté à la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="e31fa-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-131">Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong><a href="field-object-dao.md">Field</a></strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="e31fa-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-133">Définit ou renvoie une valeur qui spécifie le nom de l'objet <strong><a href="field-object-dao.md">Field</a></strong> d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="e31fa-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p104">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="e31fa-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-139">Définit ou renvoie la position relative d’un <strong><a href="field-object-dao.md">objet Field</a></strong> dans une collection <strong><a href="fields-collection-dao.md">Fields.</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-139">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection.</span></span> <span data-ttu-id="e31fa-140">.</span><span class="sxs-lookup"><span data-stu-id="e31fa-140">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-142">Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-142">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="e31fa-143"><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e31fa-143"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e31fa-144">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e31fa-144">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="e31fa-145">Renvoie la valeur d'un objet <strong>Field</strong> de la base de données qui existait au moment du lancement de la dernière mise à jour en lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="e31fa-145">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-146"><strong><a href="field-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-146"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-147">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="e31fa-147">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="e31fa-148">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e31fa-148">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-149"><strong><a href="field-required-property-dao.md">Obligatoire</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-149"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-150">Définit ou renvoie une valeur qui indique si un objet <strong><a href="field-object-dao.md">Field</a></strong> requiert une valeur non Null.</span><span class="sxs-lookup"><span data-stu-id="e31fa-150">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-151"><strong><a href="field-fieldsize-property-dao.md">Taille</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-151"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-152">Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong><a href="field-object-dao.md">Field</a></strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="e31fa-152">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p108">Renvoie une valeur spécifiant le nom du champ qui représente la source d'origine des données d'un objet <strong>Field</strong>. Type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e31fa-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p109">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet <strong>Field</strong>. Données de type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e31fa-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-159"><strong><a href="field-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-159"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-160">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="e31fa-160">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="e31fa-161"><strong>Entier</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e31fa-161">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-163">Définit ou renvoie une valeur qui spécifie si la valeur d'un objet <strong><a href="field-object-dao.md">Field</a></strong> est immédiatement validée quand la propriété <strong><a href="field-value-property-dao.md">Value</a></strong> de l'objet est définie (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="e31fa-163">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p111">Définit ou renvoie une valeur qui valide les données d'un champ lorsque ce dernier est modifié ou ajouté à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="e31fa-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-p112">Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet <strong>Field</strong> n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="e31fa-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e31fa-170"><strong><a href="field-value-property-dao.md">Valeur</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-170"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-171">Définit ou renvoie la valeur d'un objet.</span><span class="sxs-lookup"><span data-stu-id="e31fa-171">Sets or returns the value of an object.</span></span> <span data-ttu-id="e31fa-172">Type de données <strong>Variant</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e31fa-172">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e31fa-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e31fa-174">Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="e31fa-174">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="e31fa-175"><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e31fa-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e31fa-176">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e31fa-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="e31fa-177">Renvoie une valeur actuellement dans la base de données qui est plus récente que la propriété <strong>OriginalValue</strong> suite à un conflit de mise à jour en lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="e31fa-177">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

