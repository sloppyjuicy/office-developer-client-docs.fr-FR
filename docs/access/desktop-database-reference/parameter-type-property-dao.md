---
title: Parameter.Type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288020"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="2913b-102">Parameter.Type, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="2913b-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="2913b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2913b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2913b-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type **Integer** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2913b-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2913b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2913b-106">Syntax</span></span>

<span data-ttu-id="2913b-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="2913b-107">*expression* .Type</span></span>

<span data-ttu-id="2913b-108">*expression* Variable qui représente un objet **Parameter.**</span><span class="sxs-lookup"><span data-stu-id="2913b-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2913b-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="2913b-109">Remarks</span></span>

<span data-ttu-id="2913b-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **[Parameter](parameter-object-dao.md)** d'un espace de travail Microsoft Access, la propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2913b-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="2913b-112">Pour un objet **Parameter**, les paramètres et valeurs de retour possibles sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2913b-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2913b-113">Constante</span><span class="sxs-lookup"><span data-stu-id="2913b-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="2913b-114">Description</span><span class="sxs-lookup"><span data-stu-id="2913b-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2913b-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="2913b-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-118">Binary</span><span class="sxs-lookup"><span data-stu-id="2913b-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-120">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="2913b-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-122">Octet</span><span class="sxs-lookup"><span data-stu-id="2913b-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-124">Char</span><span class="sxs-lookup"><span data-stu-id="2913b-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-126">Devise</span><span class="sxs-lookup"><span data-stu-id="2913b-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="2913b-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="2913b-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-132">Double</span><span class="sxs-lookup"><span data-stu-id="2913b-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-134">Flottant</span><span class="sxs-lookup"><span data-stu-id="2913b-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-136">GUID</span><span class="sxs-lookup"><span data-stu-id="2913b-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-138">Entier</span><span class="sxs-lookup"><span data-stu-id="2913b-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-140">Entier long</span><span class="sxs-lookup"><span data-stu-id="2913b-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="2913b-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="2913b-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="2913b-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-148">Unique</span><span class="sxs-lookup"><span data-stu-id="2913b-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-150">Text</span><span class="sxs-lookup"><span data-stu-id="2913b-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-152">Time</span><span class="sxs-lookup"><span data-stu-id="2913b-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2913b-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-154">Date et heure</span><span class="sxs-lookup"><span data-stu-id="2913b-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2913b-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2913b-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2913b-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="2913b-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2913b-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="2913b-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

