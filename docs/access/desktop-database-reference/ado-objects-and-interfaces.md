---
title: Objets et interfaces ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa301974b4b417d09b0439b3970ee366eeb5d06e
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910726"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="1e29c-102">Objets et interfaces ADO</span><span class="sxs-lookup"><span data-stu-id="1e29c-102">ADO objects and interfaces</span></span>

<span data-ttu-id="1e29c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e29c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e29c-104">Les relations entre ces objets sont représentées dans le modèle d’objet ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="1e29c-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="1e29c-105">Chaque objet peut être contenu dans sa collection correspondante.</span><span class="sxs-lookup"><span data-stu-id="1e29c-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="1e29c-106">Un objet [Error](error-object-ado.md) peut, par exemple, être contenu dans une collection [Errors](errors-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1e29c-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="1e29c-107">Pour plus d’informations, consultez [collections ADO](ado-collections.md) ou une rubrique à une collection spécifique.</span><span class="sxs-lookup"><span data-stu-id="1e29c-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="1e29c-108">Objet</span><span class="sxs-lookup"><span data-stu-id="1e29c-108">Object</span></span></th>
<th><span data-ttu-id="1e29c-109">Description</span><span class="sxs-lookup"><span data-stu-id="1e29c-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e29c-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-111">Crée un objet <strong>Record</strong> ADO à partir d'un objet <strong>Row</strong> OLE DB dans une application C/C++.</span><span class="sxs-lookup"><span data-stu-id="1e29c-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e29c-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-113">Crée un objet <strong>Recordset</strong> ADO à partir d'un objet <strong>Rowset</strong> OLE DB dans une application C/C++.</span><span class="sxs-lookup"><span data-stu-id="1e29c-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e29c-114"><a href="error-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-115">Définit une commande spécifique que vous avez l'intention d'exécuter sur une source de données.</span><span class="sxs-lookup"><span data-stu-id="1e29c-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e29c-116"><a href="field-object-ado.md">Objet Connection</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-117">Représente une connexion ouverte à une source de données.</span><span class="sxs-lookup"><span data-stu-id="1e29c-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e29c-118"><a href="error-object-ado.md">Erreur</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-119">Contient des détails sur les erreurs d'accès aux données relatives à une seule opération impliquant le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1e29c-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e29c-120"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-121">Représente une colonne de données avec un type de données commun.</span><span class="sxs-lookup"><span data-stu-id="1e29c-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e29c-122"><a href="parameter-object-ado.md">Paramètre</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-123">Représente un paramètre ou un argument associé à un objet <strong>Command</strong> basé sur une requête paramétrée ou sur une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="1e29c-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e29c-124"><a href="property-object-ado.md">Propriété</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-125">Représente une caractéristique dynamique d'un objet ADO défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1e29c-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e29c-126"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-127">Représente une ligne d'un objet <strong>Recordset</strong> ou un répertoire ou un fichier dans un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1e29c-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e29c-128"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-p102">Représente le jeu entier d'enregistrements d'une table de base ou les résultats d'une commande exécutée. L'objet <strong>Recordset</strong> ne peut faire référence qu'à un seul enregistrement à l'intérieur du jeu en tant qu'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="1e29c-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e29c-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="1e29c-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="1e29c-132">Représente un flux binaire de données.</span><span class="sxs-lookup"><span data-stu-id="1e29c-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

