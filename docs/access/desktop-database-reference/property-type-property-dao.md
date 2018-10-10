---
title: Property.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c52f03d0e2fc541cb15397d0c924859cd31ccb17
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472586"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="1b738-102">Property.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b738-102">Property.Type Property (DAO)</span></span>


<span data-ttu-id="1b738-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b738-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1b738-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou de données d'un objet. Type de données **Integer** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1b738-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b738-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b738-106">Syntax</span></span>

<span data-ttu-id="1b738-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="1b738-107">*expression* .Type</span></span>

<span data-ttu-id="1b738-108">*expression* Variable qui représente un objet **Property** .</span><span class="sxs-lookup"><span data-stu-id="1b738-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b738-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b738-109">Remarks</span></span>

<span data-ttu-id="1b738-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou un type de données. Pour un objet **[Property](property-object-dao.md)**, cette propriété est en lecture-écriture jusqu'à ce que l'objet soit ajouté à une collection ou un autre objet, après quoi, elle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1b738-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="1b738-112">Les paramètres et valeurs de retour possible d'un objet **Property** sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b738-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b738-113">Constant</span><span class="sxs-lookup"><span data-stu-id="1b738-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="1b738-114">Description</span><span class="sxs-lookup"><span data-stu-id="1b738-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b738-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="1b738-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="1b738-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-120">Booléen</span><span class="sxs-lookup"><span data-stu-id="1b738-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-122">Octet</span><span class="sxs-lookup"><span data-stu-id="1b738-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-124">Char</span><span class="sxs-lookup"><span data-stu-id="1b738-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-126">Monnaie</span><span class="sxs-lookup"><span data-stu-id="1b738-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="1b738-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-129"><strong>DBDECIMAL ne</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="1b738-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-132">Double</span><span class="sxs-lookup"><span data-stu-id="1b738-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-134">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="1b738-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-136">Identificateur global unique (GUID)</span><span class="sxs-lookup"><span data-stu-id="1b738-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-138">Entier</span><span class="sxs-lookup"><span data-stu-id="1b738-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-140">Long</span><span class="sxs-lookup"><span data-stu-id="1b738-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="1b738-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="1b738-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="1b738-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-148">Simple</span><span class="sxs-lookup"><span data-stu-id="1b738-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-150">Texte</span><span class="sxs-lookup"><span data-stu-id="1b738-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-152">Heure</span><span class="sxs-lookup"><span data-stu-id="1b738-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b738-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-154">Horodatage</span><span class="sxs-lookup"><span data-stu-id="1b738-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b738-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1b738-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1b738-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="1b738-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1b738-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="1b738-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

