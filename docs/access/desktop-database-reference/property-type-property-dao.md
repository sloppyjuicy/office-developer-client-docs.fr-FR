---
title: Property.Type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302897"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="3442d-102">Property.Type, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="3442d-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="3442d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3442d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3442d-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type **Integer** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="3442d-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3442d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3442d-106">Syntax</span></span>

<span data-ttu-id="3442d-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="3442d-107">*expression* .Type</span></span>

<span data-ttu-id="3442d-108">*expression* Variable qui représente un objet **Property.**</span><span class="sxs-lookup"><span data-stu-id="3442d-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3442d-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="3442d-109">Remarks</span></span>

<span data-ttu-id="3442d-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou un type de données. Pour un objet **[Property](property-object-dao.md)**, cette propriété est en lecture-écriture jusqu'à ce que l'objet soit ajouté à une collection ou un autre objet, après quoi, elle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3442d-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="3442d-112">Les paramètres et valeurs de retour possible d'un objet **Property** sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3442d-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3442d-113">Constante</span><span class="sxs-lookup"><span data-stu-id="3442d-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="3442d-114">Description</span><span class="sxs-lookup"><span data-stu-id="3442d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3442d-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="3442d-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-118">Binary</span><span class="sxs-lookup"><span data-stu-id="3442d-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-120">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="3442d-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-122">Octet</span><span class="sxs-lookup"><span data-stu-id="3442d-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-124">Char</span><span class="sxs-lookup"><span data-stu-id="3442d-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-126">Devise</span><span class="sxs-lookup"><span data-stu-id="3442d-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="3442d-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="3442d-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-132">Double</span><span class="sxs-lookup"><span data-stu-id="3442d-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-134">Flottant</span><span class="sxs-lookup"><span data-stu-id="3442d-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-136">GUID</span><span class="sxs-lookup"><span data-stu-id="3442d-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-138">Entier</span><span class="sxs-lookup"><span data-stu-id="3442d-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-140">Entier long</span><span class="sxs-lookup"><span data-stu-id="3442d-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="3442d-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="3442d-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="3442d-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-148">Unique</span><span class="sxs-lookup"><span data-stu-id="3442d-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-150">Text</span><span class="sxs-lookup"><span data-stu-id="3442d-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-152">Time</span><span class="sxs-lookup"><span data-stu-id="3442d-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3442d-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-154">Date et heure</span><span class="sxs-lookup"><span data-stu-id="3442d-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3442d-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="3442d-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="3442d-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="3442d-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3442d-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="3442d-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

