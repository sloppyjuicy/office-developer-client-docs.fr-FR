---
title: Propriété Property. type (DAO)
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
# <a name="propertytype-property-dao"></a><span data-ttu-id="e87d4-102">Propriété Property. type (DAO)</span><span class="sxs-lookup"><span data-stu-id="e87d4-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="e87d4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e87d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e87d4-104">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="e87d4-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="e87d4-105">Type de données **Integer** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e87d4-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e87d4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e87d4-106">Syntax</span></span>

<span data-ttu-id="e87d4-107">*expression* . Entrer</span><span class="sxs-lookup"><span data-stu-id="e87d4-107">*expression* .Type</span></span>

<span data-ttu-id="e87d4-108">*expression* Variable qui représente un objet **Property** .</span><span class="sxs-lookup"><span data-stu-id="e87d4-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e87d4-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="e87d4-109">Remarks</span></span>

<span data-ttu-id="e87d4-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou un type de données. Pour un objet **[Property](property-object-dao.md)**, cette propriété est en lecture-écriture jusqu'à ce que l'objet soit ajouté à une collection ou un autre objet, après quoi, elle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e87d4-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="e87d4-112">Les paramètres et valeurs de retour possible d'un objet **Property** sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e87d4-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e87d4-113">Constante</span><span class="sxs-lookup"><span data-stu-id="e87d4-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="e87d4-114">Description</span><span class="sxs-lookup"><span data-stu-id="e87d4-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="e87d4-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="e87d4-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-120">Booléen</span><span class="sxs-lookup"><span data-stu-id="e87d4-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-122">Octet</span><span class="sxs-lookup"><span data-stu-id="e87d4-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-124">Char</span><span class="sxs-lookup"><span data-stu-id="e87d4-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-126">Monnaie</span><span class="sxs-lookup"><span data-stu-id="e87d4-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="e87d4-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="e87d4-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-132">Double</span><span class="sxs-lookup"><span data-stu-id="e87d4-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-134">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="e87d4-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-136">Identificateur global unique (GUID)</span><span class="sxs-lookup"><span data-stu-id="e87d4-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-138">Entier</span><span class="sxs-lookup"><span data-stu-id="e87d4-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-140">Long</span><span class="sxs-lookup"><span data-stu-id="e87d4-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="e87d4-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="e87d4-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="e87d4-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-148">Simple</span><span class="sxs-lookup"><span data-stu-id="e87d4-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-150">Texte</span><span class="sxs-lookup"><span data-stu-id="e87d4-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-152">Heure</span><span class="sxs-lookup"><span data-stu-id="e87d4-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87d4-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-154">Horodatage</span><span class="sxs-lookup"><span data-stu-id="e87d4-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87d4-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e87d4-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e87d4-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="e87d4-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e87d4-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="e87d4-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

