---
title: Parameter.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a1efe394193b9f8e74c02ecb71758d94fac9259a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469680"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="fe727-102">Parameter.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe727-102">Parameter.Type Property (DAO)</span></span>


<span data-ttu-id="fe727-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe727-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fe727-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou de données d'un objet. Type de données **Integer** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fe727-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe727-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe727-106">Syntax</span></span>

<span data-ttu-id="fe727-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="fe727-107">*expression* .Type</span></span>

<span data-ttu-id="fe727-108">*expression* Variable qui représente un objet **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="fe727-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe727-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe727-109">Remarks</span></span>

<span data-ttu-id="fe727-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **[Parameter](parameter-object-dao.md)** d'un espace de travail Microsoft Access, la propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fe727-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="fe727-112">Pour un objet **Parameter**, les paramètres et valeurs de retour possibles sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fe727-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe727-113">Constant</span><span class="sxs-lookup"><span data-stu-id="fe727-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="fe727-114">Description</span><span class="sxs-lookup"><span data-stu-id="fe727-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe727-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="fe727-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="fe727-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-120">Booléen</span><span class="sxs-lookup"><span data-stu-id="fe727-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-122">Octet</span><span class="sxs-lookup"><span data-stu-id="fe727-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-124">Char</span><span class="sxs-lookup"><span data-stu-id="fe727-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-126">Monnaie</span><span class="sxs-lookup"><span data-stu-id="fe727-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="fe727-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-129"><strong>DBDECIMAL ne</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="fe727-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-132">Double</span><span class="sxs-lookup"><span data-stu-id="fe727-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-134">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="fe727-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-136">Identificateur global unique (GUID)</span><span class="sxs-lookup"><span data-stu-id="fe727-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-138">Entier</span><span class="sxs-lookup"><span data-stu-id="fe727-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-140">Long</span><span class="sxs-lookup"><span data-stu-id="fe727-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="fe727-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="fe727-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="fe727-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-148">Simple</span><span class="sxs-lookup"><span data-stu-id="fe727-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-150">Texte</span><span class="sxs-lookup"><span data-stu-id="fe727-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-152">Heure</span><span class="sxs-lookup"><span data-stu-id="fe727-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe727-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-154">Horodatage</span><span class="sxs-lookup"><span data-stu-id="fe727-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe727-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="fe727-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="fe727-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="fe727-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe727-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="fe727-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

