---
title: Field2.Type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4da32f18a2b3e9dddbb0ae04e3257de34ba09761
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292663"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="fbea4-102">Field2.Type, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="fbea4-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="fbea4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbea4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbea4-104">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="fbea4-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="fbea4-105">**Entier** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fbea4-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbea4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbea4-106">Syntax</span></span>

<span data-ttu-id="fbea4-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="fbea4-107">*expression* .Type</span></span>

<span data-ttu-id="fbea4-108">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="fbea4-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbea4-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="fbea4-109">Remarks</span></span>

<span data-ttu-id="fbea4-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **Field2**, cette propriété est en lecture/écriture jusqu'à ce que l'objet soit ajouté à une collection ou à un autre objet, après quoi elle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fbea4-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="fbea4-112">Pour un objet **Field2**, les paramètres et valeurs de retour possibles sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fbea4-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbea4-113">Constante</span><span class="sxs-lookup"><span data-stu-id="fbea4-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="fbea4-114">Description</span><span class="sxs-lookup"><span data-stu-id="fbea4-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="fbea4-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-118">Binary</span><span class="sxs-lookup"><span data-stu-id="fbea4-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-120">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="fbea4-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-122">Octet</span><span class="sxs-lookup"><span data-stu-id="fbea4-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-124">Char</span><span class="sxs-lookup"><span data-stu-id="fbea4-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-126">Devise</span><span class="sxs-lookup"><span data-stu-id="fbea4-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="fbea4-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="fbea4-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-132">Double</span><span class="sxs-lookup"><span data-stu-id="fbea4-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-134">Flottant</span><span class="sxs-lookup"><span data-stu-id="fbea4-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-136">GUID</span><span class="sxs-lookup"><span data-stu-id="fbea4-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-138">Entier</span><span class="sxs-lookup"><span data-stu-id="fbea4-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-140">Entier long</span><span class="sxs-lookup"><span data-stu-id="fbea4-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="fbea4-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="fbea4-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="fbea4-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-148">Unique</span><span class="sxs-lookup"><span data-stu-id="fbea4-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-150">Text</span><span class="sxs-lookup"><span data-stu-id="fbea4-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-152">Time</span><span class="sxs-lookup"><span data-stu-id="fbea4-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbea4-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-154">Date et heure</span><span class="sxs-lookup"><span data-stu-id="fbea4-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbea4-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="fbea4-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="fbea4-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="fbea4-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fbea4-157">Lorsque vous ajoutez un nouvel objet **Field2**, **Parameter** ou **Property** à la collection d'un objet **Index**, **QueryDef**, **Recordset** ou **TableDef**, une erreur survient si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="fbea4-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

