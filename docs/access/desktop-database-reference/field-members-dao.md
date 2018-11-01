---
title: Field Members (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 649cfa4dd14ed0068aeb333ffc8e5799426ac52d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870421"
---
# <a name="field-members-dao"></a><span data-ttu-id="2bda0-102">Field Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="2bda0-102">Field Members (DAO)</span></span>


<span data-ttu-id="2bda0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bda0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2bda0-104">Un objet Field représente une colonne de données avec un type de données communes et un ensemble commun de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2bda0-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="2bda0-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2bda0-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bda0-106">Nom</span><span class="sxs-lookup"><span data-stu-id="2bda0-106">Name</span></span></p></th>
<th><p><span data-ttu-id="2bda0-107">Description</span><span class="sxs-lookup"><span data-stu-id="2bda0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-109">Ajoute des données issues d'une expression de chaîne à un objet <strong><a href="field-object-dao.md">Field</a></strong> de type mémo ou binaire long dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2bda0-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-111">Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-113">Renvoie tout ou partie du contenu d'un objet <strong><strong>Field</strong></strong> de type <a href="field-object-dao.md">Memo</a> ou <strong>Long Binary</strong> appartenant à la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2bda0-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="2bda0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2bda0-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bda0-115">Nom</span><span class="sxs-lookup"><span data-stu-id="2bda0-115">Name</span></span></p></th>
<th><p><span data-ttu-id="2bda0-116">Description</span><span class="sxs-lookup"><span data-stu-id="2bda0-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-118">Définit ou renvoie une valeur qui indique si une chaîne de longueur nulle (&quot;&quot;) est un paramètre valid pour la propriété <strong><a href="field-value-property-dao.md">Value</a></strong> de l’objet <strong><a href="field-object-dao.md">Field</a></strong> avec un type de données texte ou Mémo (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-119"><strong><a href="field-attributes-property-dao.md">Attributs</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p101">Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet <strong><a href="field-object-dao.md">Field</a></strong>. Valeur de type <strong>Long</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p101">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p102">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur <strong>Long</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-126">Renvoie une valeur qui indique si les données du champ représenté par un objet <strong><a href="field-object-dao.md">Field</a></strong> peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="2bda0-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p103">Définit ou renvoie la valeur par défaut d'un objet <strong><a href="field-object-dao.md">Field</a></strong>. Cette propriété est en lecture-écriture si l'objet <strong>Field</strong> n'est pas encore ajouté à la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-130"><strong><a href="field-fieldsize-property-dao.md">Taille du champ</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-131">Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong><a href="field-object-dao.md">Field</a></strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2bda0-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-133">Définit ou renvoie une valeur qui spécifie le nom de l'objet <strong><a href="field-object-dao.md">Field</a></strong> d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p104">Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p105">Définit ou renvoie la position relative d'un objet <strong><a href="field-object-dao.md">Field</a></strong> au sein d'une collection <strong><a href="fields-collection-dao.md">Fields</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p105">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection. .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="2bda0-p106">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="2bda0-144">Renvoie la valeur d'un objet <strong>Field</strong> de la base de données qui existait au moment du lancement de la dernière mise à jour en lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-144">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-145"><strong><a href="field-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-145"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p107">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p107">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-148"><strong><a href="field-required-property-dao.md">Obligatoire</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-148"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-149">Définit ou renvoie une valeur qui indique si un objet <strong><a href="field-object-dao.md">Field</a></strong> requiert une valeur non Null.</span><span class="sxs-lookup"><span data-stu-id="2bda0-149">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-150"><strong><a href="field-fieldsize-property-dao.md">Taille</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-150"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-151">Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong><a href="field-object-dao.md">Field</a></strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="2bda0-151">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p108">Renvoie une valeur spécifiant le nom du champ qui représente la source d'origine des données d'un objet <strong>Field</strong>. Type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p109">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet <strong>Field</strong>. Données de type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-158"><strong><a href="field-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-158"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p110">Définit ou renvoie une valeur qui indique le type opérationnel ou de données d'un objet. Type de données <strong>Integer</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p110">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-162">Définit ou renvoie une valeur qui spécifie si la valeur d'un objet <strong><a href="field-object-dao.md">Field</a></strong> est immédiatement validée quand la propriété <strong><a href="field-value-property-dao.md">Value</a></strong> de l'objet est définie (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-162">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p111">Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p112">Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet <strong>Field</strong> n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bda0-169"><strong><a href="field-value-property-dao.md">Valeur</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-169"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2bda0-p113">Définit ou renvoie la valeur d'un objet. Type de données <strong>Variant</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p113">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bda0-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="2bda0-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="2bda0-p114">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2bda0-p114">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="2bda0-175">Renvoie une valeur actuellement dans la base de données et qui est plus récente que celle de la propriété <strong>OriginalValue</strong>, ainsi que le révèle un conflit de mise à jour par lot (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="2bda0-175">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

