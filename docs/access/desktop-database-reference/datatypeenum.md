---
title: DataTypeEnum (référence de base de données du bureau Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b70ad0067083373679286bdb452cb667d3de0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471770"
---
# <a name="datatypeenum"></a><span data-ttu-id="455f8-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="455f8-102">DataTypeEnum</span></span>


<span data-ttu-id="455f8-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="455f8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="455f8-p101">Spécifie le type de données d’un [Champ](field-object-ado.md), d’un [Paramètre](parameter-object-ado.md) ou d’une [Propriété](property-object-ado.md). L’indicateur de type OLE DB correspondant est montré entre parenthèses dans la colonne Description du tableau suivant. Pour plus d’informations sur les types de données OLE DB, consultez le chapitre 13 et l’annexe A du manuel *OLE DB Programmer’s Reference*.</span><span class="sxs-lookup"><span data-stu-id="455f8-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="455f8-107">Constant</span><span class="sxs-lookup"><span data-stu-id="455f8-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="455f8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="455f8-108">Value</span></span></p></th>
<th><p><span data-ttu-id="455f8-109">Description</span><span class="sxs-lookup"><span data-stu-id="455f8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="455f8-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="455f8-110"><strong>AdArray</span></span><br /><span data-ttu-id="455f8-111">
</strong>(Ne s’applique pas à ADOX.)</span><span class="sxs-lookup"><span data-stu-id="455f8-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="455f8-112">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="455f8-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="455f8-113">Une valeur d'indicateur, toujours combinée à une autre constante de type de données, indiquant un tableau de cet autre type de données.</span><span class="sxs-lookup"><span data-stu-id="455f8-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-115">20</span><span class="sxs-lookup"><span data-stu-id="455f8-115">20</span></span></p></td>
<td><p><span data-ttu-id="455f8-116">Indique un nombre entier signé de 8 octets (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="455f8-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-118">128</span><span class="sxs-lookup"><span data-stu-id="455f8-118">128</span></span></p></td>
<td><p><span data-ttu-id="455f8-119">Indique une valeur binaire (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="455f8-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-121">11</span><span class="sxs-lookup"><span data-stu-id="455f8-121">11</span></span></p></td>
<td><p><span data-ttu-id="455f8-122">Indique une valeur de type Booléen (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="455f8-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-124">8</span><span class="sxs-lookup"><span data-stu-id="455f8-124">8</span></span></p></td>
<td><p><span data-ttu-id="455f8-125">Indique une chaîne de caractères terminée par un caractère Null (Unicode) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="455f8-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-127">136</span><span class="sxs-lookup"><span data-stu-id="455f8-127">136</span></span></p></td>
<td><p><span data-ttu-id="455f8-128">Indique une valeur de chapitre de 4 octets qui identifie les lignes dans un jeu de lignes enfant (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="455f8-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-130">129</span><span class="sxs-lookup"><span data-stu-id="455f8-130">129</span></span></p></td>
<td><p><span data-ttu-id="455f8-131">Indique une valeur de chaîne (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="455f8-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-133">6</span><span class="sxs-lookup"><span data-stu-id="455f8-133">6</span></span></p></td>
<td><p><span data-ttu-id="455f8-p102">Indique une valeur monétaire (DBTYPE_CY). Il s'agit d'un nombre à virgule fixe à 4 chiffres à droite de la virgule décimale. Il est stocké dans un nombre entier signé de 8 octets sur une échelle de 10 000.</span><span class="sxs-lookup"><span data-stu-id="455f8-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-138">7</span><span class="sxs-lookup"><span data-stu-id="455f8-138">7</span></span></p></td>
<td><p><span data-ttu-id="455f8-p103">Indique une valeur de date (DBTYPE_DATE). Une date est stockée en tant que nombre double, la partie entière étant le nombre de jours depuis le 30 décembre 1899, la partie décimale représentant la fraction d'un jour.</span><span class="sxs-lookup"><span data-stu-id="455f8-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-142">133</span><span class="sxs-lookup"><span data-stu-id="455f8-142">133</span></span></p></td>
<td><p><span data-ttu-id="455f8-143">Indique une valeur de date (aaaammjj) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="455f8-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-145">134</span><span class="sxs-lookup"><span data-stu-id="455f8-145">134</span></span></p></td>
<td><p><span data-ttu-id="455f8-146">Indique une valeur d'heure (hhmmss) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="455f8-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-148">135</span><span class="sxs-lookup"><span data-stu-id="455f8-148">135</span></span></p></td>
<td><p><span data-ttu-id="455f8-149">Indique un horodatage complet (aaaaammjjhhmmss, plus une fraction en milliardièmes) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="455f8-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-151">14</span><span class="sxs-lookup"><span data-stu-id="455f8-151">14</span></span></p></td>
<td><p><span data-ttu-id="455f8-152">Indique une valeur numérique exacte avec une précision et une échelle fixes (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="455f8-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-153"><strong>longueur fixe</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-154">5</span><span class="sxs-lookup"><span data-stu-id="455f8-154">5</span></span></p></td>
<td><p><span data-ttu-id="455f8-155">Indique une valeur à virgule flottante en double précision (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="455f8-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-157">0</span><span class="sxs-lookup"><span data-stu-id="455f8-157">0</span></span></p></td>
<td><p><span data-ttu-id="455f8-158">Ne spécifie aucune valeur (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="455f8-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-160">10</span><span class="sxs-lookup"><span data-stu-id="455f8-160">10</span></span></p></td>
<td><p><span data-ttu-id="455f8-161">Indique un code d'erreur à 32 bits (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="455f8-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-163">64</span><span class="sxs-lookup"><span data-stu-id="455f8-163">64</span></span></p></td>
<td><p><span data-ttu-id="455f8-164">Indique une valeur 64 bits représentant le nombre d'intervalles de 100 nanosecondes depuis le 1er janvier 1601 (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="455f8-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-166">72</span><span class="sxs-lookup"><span data-stu-id="455f8-166">72</span></span></p></td>
<td><p><span data-ttu-id="455f8-167">Indique un identificateur universel unique (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="455f8-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-169">9</span><span class="sxs-lookup"><span data-stu-id="455f8-169">9</span></span></p></td>
<td><p><span data-ttu-id="455f8-170">Indique un pointeur vers une interface <strong>IDispatch</strong> sur un objet COM (DBTYPE_IDISPATCH).
</span><span class="sxs-lookup"><span data-stu-id="455f8-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="455f8-p104">Ce type de données n'est pas pris en charge par ADO actuellement. Nous ne pouvons donc pas garantir leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="455f8-p104">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-173"><strong>tous les types</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-174">3</span><span class="sxs-lookup"><span data-stu-id="455f8-174">3</span></span></p></td>
<td><p><span data-ttu-id="455f8-175">Indique un nombre entier signé de 4 octets (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="455f8-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-177">13</span><span class="sxs-lookup"><span data-stu-id="455f8-177">13</span></span></p></td>
<td><p><span data-ttu-id="455f8-178">Indique un pointeur vers une interface <strong>IUnknown</strong> sur un objet COM (DBTYPE_IUNKNOWN).
</span><span class="sxs-lookup"><span data-stu-id="455f8-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="455f8-p105">Ce type de données n'est pas pris en charge par ADO actuellement. Nous ne pouvons donc pas garantir leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="455f8-p105">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-182">205</span><span class="sxs-lookup"><span data-stu-id="455f8-182">205</span></span></p></td>
<td><p><span data-ttu-id="455f8-183">Indique une valeur binaire longue.</span><span class="sxs-lookup"><span data-stu-id="455f8-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-185">201</span><span class="sxs-lookup"><span data-stu-id="455f8-185">201</span></span></p></td>
<td><p><span data-ttu-id="455f8-186">Indique une valeur de chaîne longue.</span><span class="sxs-lookup"><span data-stu-id="455f8-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-188">203</span><span class="sxs-lookup"><span data-stu-id="455f8-188">203</span></span></p></td>
<td><p><span data-ttu-id="455f8-189">Indique une valeur de chaîne longue terminée par un caractère Null (Unicode).</span><span class="sxs-lookup"><span data-stu-id="455f8-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-191">131</span><span class="sxs-lookup"><span data-stu-id="455f8-191">131</span></span></p></td>
<td><p><span data-ttu-id="455f8-192">Indique une valeur numérique exacte avec une précision et une échelle fixes (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="455f8-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-194">138</span><span class="sxs-lookup"><span data-stu-id="455f8-194">138</span></span></p></td>
<td><p><span data-ttu-id="455f8-195">Indique un PROPVARIANT d'automatisation (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="455f8-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-197">4</span><span class="sxs-lookup"><span data-stu-id="455f8-197">4</span></span></p></td>
<td><p><span data-ttu-id="455f8-198">Indique une valeur à virgule flottante en simple précision (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="455f8-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-200">2</span><span class="sxs-lookup"><span data-stu-id="455f8-200">2</span></span></p></td>
<td><p><span data-ttu-id="455f8-201">Indique un nombre entier signé de 2 octets (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="455f8-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-203">16</span><span class="sxs-lookup"><span data-stu-id="455f8-203">16</span></span></p></td>
<td><p><span data-ttu-id="455f8-204">Indique un nombre entier signé de 1 octet (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="455f8-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-206">21</span><span class="sxs-lookup"><span data-stu-id="455f8-206">21</span></span></p></td>
<td><p><span data-ttu-id="455f8-207">Indique un nombre entier non signé de 8 octets (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="455f8-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-209">19</span><span class="sxs-lookup"><span data-stu-id="455f8-209">19</span></span></p></td>
<td><p><span data-ttu-id="455f8-210">Indique un nombre entier non signé de 8 octets (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="455f8-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-212">18</span><span class="sxs-lookup"><span data-stu-id="455f8-212">18</span></span></p></td>
<td><p><span data-ttu-id="455f8-213">Indique un nombre entier non signé de 2 octets (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="455f8-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-215">17</span><span class="sxs-lookup"><span data-stu-id="455f8-215">17</span></span></p></td>
<td><p><span data-ttu-id="455f8-216">Indique un nombre entier non signé de 1 octet (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="455f8-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-218">132</span><span class="sxs-lookup"><span data-stu-id="455f8-218">132</span></span></p></td>
<td><p><span data-ttu-id="455f8-219">Indique une variable définie par l'utilisateur (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="455f8-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-221">204</span><span class="sxs-lookup"><span data-stu-id="455f8-221">204</span></span></p></td>
<td><p><span data-ttu-id="455f8-222">Indique une valeur binaire (objet <strong>Parameter</strong> uniquement).</span><span class="sxs-lookup"><span data-stu-id="455f8-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-224">200</span><span class="sxs-lookup"><span data-stu-id="455f8-224">200</span></span></p></td>
<td><p><span data-ttu-id="455f8-225">Indique une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="455f8-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-227">12</span><span class="sxs-lookup"><span data-stu-id="455f8-227">12</span></span></p></td>
<td><p><span data-ttu-id="455f8-228">Indique un objet <strong>Variant</strong> d'automatisation (DBTYPE_VARIANT).
</span><span class="sxs-lookup"><span data-stu-id="455f8-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="455f8-p106">Ce type de données n'est pas pris en charge par ADO actuellement. Nous ne pouvons donc pas garantir leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="455f8-p106">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-232">139</span><span class="sxs-lookup"><span data-stu-id="455f8-232">139</span></span></p></td>
<td><p><span data-ttu-id="455f8-233">Indique une valeur numérique (objet <strong>Parameter</strong> uniquement).</span><span class="sxs-lookup"><span data-stu-id="455f8-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-235">202</span><span class="sxs-lookup"><span data-stu-id="455f8-235">202</span></span></p></td>
<td><p><span data-ttu-id="455f8-236">Indique une chaîne de caractères terminée par un caractère Null (Unicode).</span><span class="sxs-lookup"><span data-stu-id="455f8-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="455f8-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="455f8-238">130</span><span class="sxs-lookup"><span data-stu-id="455f8-238">130</span></span></p></td>
<td><p><span data-ttu-id="455f8-239">Indique une chaîne de caractères terminée par un caractère Null (Unicode) (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="455f8-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="455f8-240">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="455f8-240">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="455f8-241">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="455f8-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="455f8-242">Constante</span><span class="sxs-lookup"><span data-stu-id="455f8-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="455f8-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="455f8-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="455f8-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="455f8-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="455f8-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="455f8-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="455f8-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="455f8-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="455f8-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="455f8-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="455f8-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="455f8-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="455f8-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="455f8-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="455f8-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="455f8-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="455f8-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="455f8-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="455f8-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="455f8-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="455f8-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="455f8-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="455f8-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="455f8-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="455f8-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="455f8-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="455f8-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="455f8-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="455f8-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="455f8-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="455f8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="455f8-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="455f8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="455f8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="455f8-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="455f8-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="455f8-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="455f8-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="455f8-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="455f8-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="455f8-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="455f8-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="455f8-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

