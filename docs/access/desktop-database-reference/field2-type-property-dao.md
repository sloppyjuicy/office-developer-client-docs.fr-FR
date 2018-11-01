---
title: Field2.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1ebb10e2a9248ec38d49a874cf319c3120cd009
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877001"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="15cb8-102">Field2.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="15cb8-102">Field2.Type Property (DAO)</span></span>


<span data-ttu-id="15cb8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15cb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15cb8-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou de données d'un objet. Type de données **Integer** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="15cb8-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="15cb8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15cb8-106">Syntax</span></span>

<span data-ttu-id="15cb8-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="15cb8-107">*expression* .Type</span></span>

<span data-ttu-id="15cb8-108">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="15cb8-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="15cb8-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="15cb8-109">Remarks</span></span>

<span data-ttu-id="15cb8-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **Field2**, cette propriété est en lecture/écriture jusqu'à ce que l'objet soit ajouté à une collection ou à un autre objet, après quoi elle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="15cb8-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="15cb8-112">Pour un objet **Field2**, les paramètres et valeurs de retour possibles sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="15cb8-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15cb8-113">Constant</span><span class="sxs-lookup"><span data-stu-id="15cb8-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="15cb8-114">Description</span><span class="sxs-lookup"><span data-stu-id="15cb8-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="15cb8-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="15cb8-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-120">Booléen</span><span class="sxs-lookup"><span data-stu-id="15cb8-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-122">Octet</span><span class="sxs-lookup"><span data-stu-id="15cb8-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-124">Char</span><span class="sxs-lookup"><span data-stu-id="15cb8-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-126">Monnaie</span><span class="sxs-lookup"><span data-stu-id="15cb8-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="15cb8-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-129"><strong>DBDECIMAL ne</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="15cb8-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-132">Double</span><span class="sxs-lookup"><span data-stu-id="15cb8-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-134">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="15cb8-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-136">Identificateur global unique (GUID)</span><span class="sxs-lookup"><span data-stu-id="15cb8-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-138">Entier</span><span class="sxs-lookup"><span data-stu-id="15cb8-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-140">Long</span><span class="sxs-lookup"><span data-stu-id="15cb8-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="15cb8-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="15cb8-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="15cb8-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-148">Simple</span><span class="sxs-lookup"><span data-stu-id="15cb8-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-150">Texte</span><span class="sxs-lookup"><span data-stu-id="15cb8-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-152">Heure</span><span class="sxs-lookup"><span data-stu-id="15cb8-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15cb8-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-154">Horodatage</span><span class="sxs-lookup"><span data-stu-id="15cb8-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15cb8-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="15cb8-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="15cb8-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="15cb8-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15cb8-157">Lorsque vous ajoutez un nouvel objet **Field2**, **Parameter** ou **Property** à la collection d'un objet **Index**, **QueryDef**, **Recordset** ou **TableDef**, une erreur survient si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="15cb8-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

