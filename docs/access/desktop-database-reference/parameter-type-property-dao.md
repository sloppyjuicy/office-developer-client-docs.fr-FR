---
title: Propriété Parameter.Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 294d61ba964958d7933a68919df940cb7501ec0d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927031"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="f12d1-102">Propriété Parameter.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="f12d1-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="f12d1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f12d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f12d1-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou de données d'un objet. Type de données **Integer** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f12d1-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f12d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f12d1-106">Syntax</span></span>

<span data-ttu-id="f12d1-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="f12d1-107">*expression* .Type</span></span>

<span data-ttu-id="f12d1-108">*expression* Variable qui représente un objet **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="f12d1-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f12d1-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f12d1-109">Remarks</span></span>

<span data-ttu-id="f12d1-p102">Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **[Parameter](parameter-object-dao.md)** d'un espace de travail Microsoft Access, la propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f12d1-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="f12d1-112">Pour un objet **Parameter**, les paramètres et valeurs de retour possibles sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f12d1-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f12d1-113">Constant</span><span class="sxs-lookup"><span data-stu-id="f12d1-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="f12d1-114">Description</span><span class="sxs-lookup"><span data-stu-id="f12d1-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-116">Entier très grand</span><span class="sxs-lookup"><span data-stu-id="f12d1-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="f12d1-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-120">Booléen</span><span class="sxs-lookup"><span data-stu-id="f12d1-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-122">Octet</span><span class="sxs-lookup"><span data-stu-id="f12d1-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-124">Char</span><span class="sxs-lookup"><span data-stu-id="f12d1-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-126">Monnaie</span><span class="sxs-lookup"><span data-stu-id="f12d1-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-128">Date/Heure</span><span class="sxs-lookup"><span data-stu-id="f12d1-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-129"><strong>DBDECIMAL ne</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-130">Décimal</span><span class="sxs-lookup"><span data-stu-id="f12d1-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-132">Double</span><span class="sxs-lookup"><span data-stu-id="f12d1-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-134">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="f12d1-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-136">Identificateur global unique (GUID)</span><span class="sxs-lookup"><span data-stu-id="f12d1-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-138">Entier</span><span class="sxs-lookup"><span data-stu-id="f12d1-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-140">Long</span><span class="sxs-lookup"><span data-stu-id="f12d1-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-142">Binaire long (objet OLE)</span><span class="sxs-lookup"><span data-stu-id="f12d1-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-144">Mémo</span><span class="sxs-lookup"><span data-stu-id="f12d1-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-146">Numérique</span><span class="sxs-lookup"><span data-stu-id="f12d1-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-148">Simple</span><span class="sxs-lookup"><span data-stu-id="f12d1-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-150">Texte</span><span class="sxs-lookup"><span data-stu-id="f12d1-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-152">Heure</span><span class="sxs-lookup"><span data-stu-id="f12d1-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f12d1-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-154">Horodatage</span><span class="sxs-lookup"><span data-stu-id="f12d1-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f12d1-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f12d1-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f12d1-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="f12d1-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f12d1-157">Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f12d1-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

