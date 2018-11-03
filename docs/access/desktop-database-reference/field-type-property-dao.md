---
title: Propriété Field.Type (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f532897ca20dda7b8ca82d831398e20cfa6b9da
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923153"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="4553f-102">Propriété Field.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="4553f-102">Field.Type property (DAO)</span></span>


<span data-ttu-id="4553f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4553f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4553f-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou de données d'un objet. Type de données **Integer** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4553f-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4553f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4553f-106">Syntax</span></span>

<span data-ttu-id="4553f-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="4553f-107">*expression* .Type</span></span>

<span data-ttu-id="4553f-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="4553f-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4553f-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="4553f-109">Remarks</span></span>

<span data-ttu-id="4553f-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **Field**, cette propriété est en lecture/écriture jusqu'à ce que l'objet soit ajouté à une collection ou à un autre objet ; elle passe alors en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4553f-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="4553f-112">Pour un objet **Field**, les valeurs des paramètres et de retour possibles sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4553f-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4553f-113">Constant</span><span class="sxs-lookup"><span data-stu-id="4553f-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="4553f-114">Description</span><span class="sxs-lookup"><span data-stu-id="4553f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4553f-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="4553f-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="4553f-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-120">Booléen</span><span class="sxs-lookup"><span data-stu-id="4553f-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-122">Octet</span><span class="sxs-lookup"><span data-stu-id="4553f-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-124">Char</span><span class="sxs-lookup"><span data-stu-id="4553f-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-126">Monnaie</span><span class="sxs-lookup"><span data-stu-id="4553f-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="4553f-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-129"><strong>DBDECIMAL ne</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="4553f-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-132">Double</span><span class="sxs-lookup"><span data-stu-id="4553f-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-134">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="4553f-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-136">Identificateur global unique (GUID)</span><span class="sxs-lookup"><span data-stu-id="4553f-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-138">Entier</span><span class="sxs-lookup"><span data-stu-id="4553f-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-140">Long</span><span class="sxs-lookup"><span data-stu-id="4553f-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="4553f-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="4553f-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="4553f-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-148">Simple</span><span class="sxs-lookup"><span data-stu-id="4553f-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-150">Texte</span><span class="sxs-lookup"><span data-stu-id="4553f-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-152">Heure</span><span class="sxs-lookup"><span data-stu-id="4553f-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4553f-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-154">Horodatage</span><span class="sxs-lookup"><span data-stu-id="4553f-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4553f-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4553f-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4553f-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="4553f-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4553f-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="4553f-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

