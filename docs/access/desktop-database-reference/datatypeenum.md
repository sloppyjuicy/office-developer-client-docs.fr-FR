---
title: DataTypeEnum (référence de base de données de bureau Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294441"
---
# <a name="datatypeenum"></a><span data-ttu-id="9aba9-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="9aba9-102">DataTypeEnum</span></span>

<span data-ttu-id="9aba9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aba9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9aba9-p101">Spécifie le type de données d’un [Champ](field-object-ado.md), d’un [Paramètre](parameter-object-ado.md) ou d’une [Propriété](property-object-ado.md). L’indicateur de type OLE DB correspondant est montré entre parenthèses dans la colonne Description du tableau suivant. Pour plus d’informations sur les types de données OLE DB, consultez le chapitre 13 et l’annexe A du manuel *OLE DB Programmer’s Reference*.</span><span class="sxs-lookup"><span data-stu-id="9aba9-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9aba9-107">Constante</span><span class="sxs-lookup"><span data-stu-id="9aba9-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="9aba9-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9aba9-108">Value</span></span></p></th>
<th><p><span data-ttu-id="9aba9-109">Description</span><span class="sxs-lookup"><span data-stu-id="9aba9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="9aba9-110"><strong>AdArray</span></span><br /><span data-ttu-id="9aba9-111">
</strong>(Ne s'applique pas à ADOX.)</span><span class="sxs-lookup"><span data-stu-id="9aba9-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="9aba9-112">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="9aba9-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="9aba9-113">Une valeur d'indicateur, toujours combinée à une autre constante de type de données, indiquant un tableau de cet autre type de données.</span><span class="sxs-lookup"><span data-stu-id="9aba9-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-115">vingtaine</span><span class="sxs-lookup"><span data-stu-id="9aba9-115">20</span></span></p></td>
<td><p><span data-ttu-id="9aba9-116">Indique un nombre entier signé de 8 octets (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="9aba9-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-118">128</span><span class="sxs-lookup"><span data-stu-id="9aba9-118">128</span></span></p></td>
<td><p><span data-ttu-id="9aba9-119">Indique une valeur binaire (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="9aba9-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-121">a4</span><span class="sxs-lookup"><span data-stu-id="9aba9-121">11</span></span></p></td>
<td><p><span data-ttu-id="9aba9-122">Indique une valeur de type Booléen (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="9aba9-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-124">8bits</span><span class="sxs-lookup"><span data-stu-id="9aba9-124">8</span></span></p></td>
<td><p><span data-ttu-id="9aba9-125">Indique une chaîne de caractères terminée par un caractère Null (Unicode) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="9aba9-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-127">136</span><span class="sxs-lookup"><span data-stu-id="9aba9-127">136</span></span></p></td>
<td><p><span data-ttu-id="9aba9-128">Indique une valeur de chapitre de 4 octets qui identifie les lignes dans un jeu de lignes enfant (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="9aba9-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-130">129</span><span class="sxs-lookup"><span data-stu-id="9aba9-130">129</span></span></p></td>
<td><p><span data-ttu-id="9aba9-131">Indique une valeur de chaîne (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="9aba9-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-133">6.x</span><span class="sxs-lookup"><span data-stu-id="9aba9-133">6</span></span></p></td>
<td><p><span data-ttu-id="9aba9-p102">Indique une valeur monétaire (DBTYPE_CY). Il s'agit d'un nombre à virgule fixe à 4 chiffres à droite de la virgule décimale. Il est stocké dans un nombre entier signé de 8 octets sur une échelle de 10 000.</span><span class="sxs-lookup"><span data-stu-id="9aba9-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-138">7j/7</span><span class="sxs-lookup"><span data-stu-id="9aba9-138">7</span></span></p></td>
<td><p><span data-ttu-id="9aba9-p103">Indique une valeur de date (DBTYPE_DATE). Une date est stockée en tant que nombre double, la partie entière étant le nombre de jours depuis le 30 décembre 1899, la partie décimale représentant la fraction d'un jour.</span><span class="sxs-lookup"><span data-stu-id="9aba9-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-142">133</span><span class="sxs-lookup"><span data-stu-id="9aba9-142">133</span></span></p></td>
<td><p><span data-ttu-id="9aba9-143">Indique une valeur de date (aaaammjj) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="9aba9-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-145">134</span><span class="sxs-lookup"><span data-stu-id="9aba9-145">134</span></span></p></td>
<td><p><span data-ttu-id="9aba9-146">Indique une valeur d'heure (hhmmss) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="9aba9-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-148">135</span><span class="sxs-lookup"><span data-stu-id="9aba9-148">135</span></span></p></td>
<td><p><span data-ttu-id="9aba9-149">Indique un horodatage complet (aaaaammjjhhmmss, plus une fraction en milliardièmes) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="9aba9-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-151">13</span><span class="sxs-lookup"><span data-stu-id="9aba9-151">14</span></span></p></td>
<td><p><span data-ttu-id="9aba9-152">Indique une valeur numérique exacte avec une précision et une échelle fixes (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="9aba9-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-154">disque</span><span class="sxs-lookup"><span data-stu-id="9aba9-154">5</span></span></p></td>
<td><p><span data-ttu-id="9aba9-155">Indique une valeur à virgule flottante en double précision (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="9aba9-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-157">0</span><span class="sxs-lookup"><span data-stu-id="9aba9-157">0</span></span></p></td>
<td><p><span data-ttu-id="9aba9-158">Ne spécifie aucune valeur (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="9aba9-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-160">10</span><span class="sxs-lookup"><span data-stu-id="9aba9-160">10</span></span></p></td>
<td><p><span data-ttu-id="9aba9-161">Indique un code d'erreur à 32 bits (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="9aba9-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-163">64</span><span class="sxs-lookup"><span data-stu-id="9aba9-163">64</span></span></p></td>
<td><p><span data-ttu-id="9aba9-164">Indique une valeur 64 bits représentant le nombre d'intervalles de 100 nanosecondes depuis le 1er janvier 1601 (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="9aba9-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-166">72</span><span class="sxs-lookup"><span data-stu-id="9aba9-166">72</span></span></p></td>
<td><p><span data-ttu-id="9aba9-167">Indique un identificateur universel unique (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="9aba9-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-169">4,9</span><span class="sxs-lookup"><span data-stu-id="9aba9-169">9</span></span></p></td>
<td><p><span data-ttu-id="9aba9-170">Indique un pointeur vers une interface <strong>IDispatch</strong> sur un objet COM (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="9aba9-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="9aba9-171"><strong>Remarque</strong>: ce type de données n'est pas pris en charge actuellement par ADO.</span><span class="sxs-lookup"><span data-stu-id="9aba9-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="9aba9-172">Nous ne pouvons donc pas garantir leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="9aba9-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-174">3</span><span class="sxs-lookup"><span data-stu-id="9aba9-174">3</span></span></p></td>
<td><p><span data-ttu-id="9aba9-175">Indique un nombre entier signé de 4 octets (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="9aba9-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-177">kg</span><span class="sxs-lookup"><span data-stu-id="9aba9-177">13</span></span></p></td>
<td><p><span data-ttu-id="9aba9-178">Indique un pointeur vers une interface <strong>IUnknown</strong> sur un objet COM (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="9aba9-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="9aba9-179"><strong>Remarque</strong>: ce type de données n'est pas pris en charge actuellement par ADO.</span><span class="sxs-lookup"><span data-stu-id="9aba9-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="9aba9-180">Nous ne pouvons donc pas garantir leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="9aba9-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-182">205</span><span class="sxs-lookup"><span data-stu-id="9aba9-182">205</span></span></p></td>
<td><p><span data-ttu-id="9aba9-183">Indique une valeur binaire longue.</span><span class="sxs-lookup"><span data-stu-id="9aba9-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-185">201</span><span class="sxs-lookup"><span data-stu-id="9aba9-185">201</span></span></p></td>
<td><p><span data-ttu-id="9aba9-186">Indique une valeur de chaîne longue.</span><span class="sxs-lookup"><span data-stu-id="9aba9-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-188">203</span><span class="sxs-lookup"><span data-stu-id="9aba9-188">203</span></span></p></td>
<td><p><span data-ttu-id="9aba9-189">Indique une valeur de chaîne longue terminée par un caractère Null (Unicode).</span><span class="sxs-lookup"><span data-stu-id="9aba9-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-191">131</span><span class="sxs-lookup"><span data-stu-id="9aba9-191">131</span></span></p></td>
<td><p><span data-ttu-id="9aba9-192">Indique une valeur numérique exacte avec une précision et une échelle fixes (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="9aba9-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-194">138</span><span class="sxs-lookup"><span data-stu-id="9aba9-194">138</span></span></p></td>
<td><p><span data-ttu-id="9aba9-195">Indique un PROPVARIANT d'automatisation (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="9aba9-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-197">4</span><span class="sxs-lookup"><span data-stu-id="9aba9-197">4</span></span></p></td>
<td><p><span data-ttu-id="9aba9-198">Indique une valeur à virgule flottante en simple précision (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="9aba9-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-200">n°2</span><span class="sxs-lookup"><span data-stu-id="9aba9-200">2</span></span></p></td>
<td><p><span data-ttu-id="9aba9-201">Indique un nombre entier signé de 2 octets (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="9aba9-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-203">Seiz</span><span class="sxs-lookup"><span data-stu-id="9aba9-203">16</span></span></p></td>
<td><p><span data-ttu-id="9aba9-204">Indique un nombre entier signé de 1 octet (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="9aba9-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-206">21</span><span class="sxs-lookup"><span data-stu-id="9aba9-206">21</span></span></p></td>
<td><p><span data-ttu-id="9aba9-207">Indique un nombre entier non signé de 8 octets (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="9aba9-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-209">neuf</span><span class="sxs-lookup"><span data-stu-id="9aba9-209">19</span></span></p></td>
<td><p><span data-ttu-id="9aba9-210">Indique un nombre entier non signé de 8 octets (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="9aba9-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-212">18</span><span class="sxs-lookup"><span data-stu-id="9aba9-212">18</span></span></p></td>
<td><p><span data-ttu-id="9aba9-213">Indique un nombre entier non signé de 2 octets (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="9aba9-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-215">cm</span><span class="sxs-lookup"><span data-stu-id="9aba9-215">17</span></span></p></td>
<td><p><span data-ttu-id="9aba9-216">Indique un nombre entier non signé de 1 octet (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="9aba9-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-218">132</span><span class="sxs-lookup"><span data-stu-id="9aba9-218">132</span></span></p></td>
<td><p><span data-ttu-id="9aba9-219">Indique une variable définie par l'utilisateur (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="9aba9-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-221">204</span><span class="sxs-lookup"><span data-stu-id="9aba9-221">204</span></span></p></td>
<td><p><span data-ttu-id="9aba9-222">Indique une valeur binaire (objet <strong>Parameter</strong> uniquement).</span><span class="sxs-lookup"><span data-stu-id="9aba9-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-224">200</span><span class="sxs-lookup"><span data-stu-id="9aba9-224">200</span></span></p></td>
<td><p><span data-ttu-id="9aba9-225">Indique une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9aba9-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-227">an</span><span class="sxs-lookup"><span data-stu-id="9aba9-227">12</span></span></p></td>
<td><p><span data-ttu-id="9aba9-228">Indique un objet <strong>Variant</strong> d'automatisation (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="9aba9-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="9aba9-229"><strong>Remarque</strong>: ce type de données n'est pas pris en charge actuellement par ADO.</span><span class="sxs-lookup"><span data-stu-id="9aba9-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="9aba9-230">Nous ne pouvons donc pas garantir leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="9aba9-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-232">139</span><span class="sxs-lookup"><span data-stu-id="9aba9-232">139</span></span></p></td>
<td><p><span data-ttu-id="9aba9-233">Indique une valeur numérique (objet <strong>Parameter</strong> uniquement).</span><span class="sxs-lookup"><span data-stu-id="9aba9-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-235">202</span><span class="sxs-lookup"><span data-stu-id="9aba9-235">202</span></span></p></td>
<td><p><span data-ttu-id="9aba9-236">Indique une chaîne de caractères terminée par un caractère Null (Unicode).</span><span class="sxs-lookup"><span data-stu-id="9aba9-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="9aba9-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9aba9-238">130</span><span class="sxs-lookup"><span data-stu-id="9aba9-238">130</span></span></p></td>
<td><p><span data-ttu-id="9aba9-239">Indique une chaîne de caractères terminée par un caractère Null (Unicode) (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="9aba9-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9aba9-240">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9aba9-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="9aba9-241">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9aba9-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9aba9-242">Constante</span><span class="sxs-lookup"><span data-stu-id="9aba9-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-243">AdoEnums. DataType. ARRAY</span><span class="sxs-lookup"><span data-stu-id="9aba9-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-244">AdoEnums. DataType. BIGINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-245">AdoEnums. DataType. BINARY</span><span class="sxs-lookup"><span data-stu-id="9aba9-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-246">AdoEnums. DataType. BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9aba9-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-247">AdoEnums. DataType. BSTR</span><span class="sxs-lookup"><span data-stu-id="9aba9-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-248">AdoEnums. DataType. CHAPTER</span><span class="sxs-lookup"><span data-stu-id="9aba9-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-249">AdoEnums. DataType. CHAR</span><span class="sxs-lookup"><span data-stu-id="9aba9-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-250">AdoEnums. DataType. CURRENCY</span><span class="sxs-lookup"><span data-stu-id="9aba9-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-251">AdoEnums. DataType. DATE</span><span class="sxs-lookup"><span data-stu-id="9aba9-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-252">AdoEnums. DataType. DBDATE</span><span class="sxs-lookup"><span data-stu-id="9aba9-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-253">AdoEnums. DataType. DBTIME</span><span class="sxs-lookup"><span data-stu-id="9aba9-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-254">AdoEnums. DataType. DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="9aba9-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-255">AdoEnums. DataType. DECIMAL</span><span class="sxs-lookup"><span data-stu-id="9aba9-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-256">AdoEnums. DataType. DOUBLE</span><span class="sxs-lookup"><span data-stu-id="9aba9-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-257">AdoEnums. DataType. EMPTY</span><span class="sxs-lookup"><span data-stu-id="9aba9-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-258">AdoEnums. DataType. ERROR</span><span class="sxs-lookup"><span data-stu-id="9aba9-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-259">AdoEnums. DataType. FILETIME</span><span class="sxs-lookup"><span data-stu-id="9aba9-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-260">AdoEnums. DataType. GUID</span><span class="sxs-lookup"><span data-stu-id="9aba9-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-261">AdoEnums. DataType. IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="9aba9-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-262">AdoEnums. DataType. INTEGER</span><span class="sxs-lookup"><span data-stu-id="9aba9-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-263">AdoEnums. DataType. IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="9aba9-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-264">AdoEnums. DataType. LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="9aba9-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-265">AdoEnums. DataType. LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="9aba9-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-266">AdoEnums. DataType. LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="9aba9-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-267">AdoEnums. DataType. NUMERIC</span><span class="sxs-lookup"><span data-stu-id="9aba9-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-268">AdoEnums. DataType. PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9aba9-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-269">AdoEnums. DataType. SINGLE</span><span class="sxs-lookup"><span data-stu-id="9aba9-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-270">AdoEnums. DataType. SMALLINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-271">AdoEnums. DataType. TINYINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-272">AdoEnums. DataType. UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-273">AdoEnums. DataType. UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-274">AdoEnums. DataType. UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-275">AdoEnums. DataType. UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="9aba9-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-276">AdoEnums. DataType. USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="9aba9-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-277">AdoEnums. DataType. VARBINARY</span><span class="sxs-lookup"><span data-stu-id="9aba9-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-278">AdoEnums. DataType. VARCHAR</span><span class="sxs-lookup"><span data-stu-id="9aba9-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-279">AdoEnums. DataType. VARIANT</span><span class="sxs-lookup"><span data-stu-id="9aba9-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-280">AdoEnums. DataType. VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="9aba9-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aba9-281">AdoEnums. DataType. VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="9aba9-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aba9-282">AdoEnums. DataType. WCHAR</span><span class="sxs-lookup"><span data-stu-id="9aba9-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

