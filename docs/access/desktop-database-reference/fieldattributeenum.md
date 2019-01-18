---
title: FieldAttributeEnum (référence de base de données du bureau Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706876"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="cf0a9-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="cf0a9-102">FieldAttributeEnum</span></span>

<span data-ttu-id="cf0a9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf0a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf0a9-104">Spécifie un ou plusieurs attributs d'un objet [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cf0a9-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf0a9-105">Constante</span><span class="sxs-lookup"><span data-stu-id="cf0a9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cf0a9-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf0a9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cf0a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="cf0a9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="cf0a9-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-110">Indique que le fournisseur met en mémoire cache les valeurs des champs et que les lectures suivantes sont effectuées depuis la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-112">0 x 10</span><span class="sxs-lookup"><span data-stu-id="cf0a9-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-113">Indique que le champ contient des données de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-115">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="cf0a9-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-p101">Indique que le champ contient une valeur de chapitre, qui spécifie un recordset enfant lié à ce champ parent. En général, les champs de chapitre sont utilisés avec le service Data Shaping ou les filtres.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-p101">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field. Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-119">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="cf0a9-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-120">Indique que le champ spécifie que la ressource représentée par l'enregistrement est une collection d'autres ressources, comme un dossier, plutôt que comme une ressource simple comme un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-122">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="cf0a9-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-123">Indique que le champ contient le flux par défaut pour la ressource représentée par l’objet record.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="cf0a9-124">Par exemple, le flux par défaut peut être le contenu HTML d’un dossier racine sur un site Web, qui est automatiquement servi lorsque l’URL racine est spécifié.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-126">0 x 20</span><span class="sxs-lookup"><span data-stu-id="cf0a9-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-127">Indique que le champ accepte des valeurs nulles.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-129">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="cf0a9-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-130">Indique que le champ contient l'URL qui appelle la ressource à partir de l'emplacement des données représenté par l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-132">0 x 80</span><span class="sxs-lookup"><span data-stu-id="cf0a9-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-p103">Indique que le champ est de type binaire long. Indique également que vous pouvez utiliser les méthodes <a href="appendchunk-method-ado.md">AppendChunk</a> et <a href="getchunk-method-ado.md">GetChunk</a>.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-p103">Indicates that the field is a long binary field. Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-136">0 x 40</span><span class="sxs-lookup"><span data-stu-id="cf0a9-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-137">Indique que vous pouvez lire des valeurs nulles à partir du champ.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-139">0x2</span><span class="sxs-lookup"><span data-stu-id="cf0a9-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-140">Indique que le champ est différé : ses valeurs ne sont pas extraites de la source de données avec l'intégralité de l'enregistrement, mais seulement lors d'un accès explicite de votre part.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="cf0a9-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-p104">Indique que le champ représente une valeur numérique depuis une colonne qui prend en charge les valeurs d’échelle négatives. L’échelle est spécifiée par la propriété <a href="numericscale-property-ado.md">NumericScale</a>.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-p104">Indicates that the field represents a numeric value from a column that supports negative scale values. The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-146">0 x 100</span><span class="sxs-lookup"><span data-stu-id="cf0a9-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-147">Indique que le champ contient un identificateur de lignes persistantes sur lequel il n'est pas possible d'écrire et qui ne possède pas de valeurs significatives, sauf pour l'identification de la ligne (comme un numéro d'enregistrement, un identificateur unique, etc.).</span><span class="sxs-lookup"><span data-stu-id="cf0a9-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-149">0 x 200</span><span class="sxs-lookup"><span data-stu-id="cf0a9-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-150">Indique que le champ contient un horodatage (heure ou date) utilisé pour suivre les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-152">0 x 8</span><span class="sxs-lookup"><span data-stu-id="cf0a9-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-153">Indique que le fournisseur ne peut déterminer si vous pouvez écrire dans le champ.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-155">-1</span><span class="sxs-lookup"><span data-stu-id="cf0a9-155">-1</span></span><br />
<span data-ttu-id="cf0a9-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cf0a9-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-157">Indique que le fournisseur ne spécifie pas d'attributs pour le champ.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="cf0a9-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="cf0a9-159">0 x 4</span><span class="sxs-lookup"><span data-stu-id="cf0a9-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="cf0a9-160">Indique que vous pouvez écrire dans le champ.</span><span class="sxs-lookup"><span data-stu-id="cf0a9-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cf0a9-161">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="cf0a9-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="cf0a9-162">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cf0a9-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf0a9-163">Constante</span><span class="sxs-lookup"><span data-stu-id="cf0a9-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="cf0a9-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="cf0a9-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="cf0a9-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="cf0a9-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="cf0a9-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="cf0a9-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="cf0a9-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="cf0a9-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="cf0a9-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="cf0a9-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf0a9-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="cf0a9-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf0a9-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="cf0a9-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

