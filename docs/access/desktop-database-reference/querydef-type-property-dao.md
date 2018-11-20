---
title: Propriété QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd958c4b2123c727c3bc0a14a067fcb719ec86b3
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026385"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="ee7af-102">Propriété QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="ee7af-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="ee7af-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee7af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee7af-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ee7af-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7af-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee7af-106">Syntax</span></span>

<span data-ttu-id="ee7af-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="ee7af-107">*expression* .Type</span></span>

<span data-ttu-id="ee7af-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="ee7af-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee7af-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee7af-109">Remarks</span></span>

<span data-ttu-id="ee7af-110">Les paramètres et valeurs de retour possible d'un objet **QueryDef** sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ee7af-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee7af-111">Constante</span><span class="sxs-lookup"><span data-stu-id="ee7af-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="ee7af-112">Type de requête</span><span class="sxs-lookup"><span data-stu-id="ee7af-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-114">Opération</span><span class="sxs-lookup"><span data-stu-id="ee7af-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7af-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-116">Ajout</span><span class="sxs-lookup"><span data-stu-id="ee7af-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-118">Composé</span><span class="sxs-lookup"><span data-stu-id="ee7af-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7af-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-120">Analyse croisée</span><span class="sxs-lookup"><span data-stu-id="ee7af-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-122">Définition de données</span><span class="sxs-lookup"><span data-stu-id="ee7af-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7af-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-124">Delete</span><span class="sxs-lookup"><span data-stu-id="ee7af-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-126">Création de table</span><span class="sxs-lookup"><span data-stu-id="ee7af-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7af-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-128">Procédure (espaces de travail ODBCDirect uniquement)</span><span class="sxs-lookup"><span data-stu-id="ee7af-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="ee7af-129"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="ee7af-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="ee7af-130">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ee7af-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-132">Sélection</span><span class="sxs-lookup"><span data-stu-id="ee7af-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7af-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-134">Union</span><span class="sxs-lookup"><span data-stu-id="ee7af-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-136">Utilisé avec <strong>dbQSQLPassThrough</strong> pour spécifier une requête qui ne renvoie pas d’enregistrements (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ee7af-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7af-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-138">Requête SQL directe (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="ee7af-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7af-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="ee7af-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7af-140">Update</span><span class="sxs-lookup"><span data-stu-id="ee7af-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee7af-141">Lorsque vous ajoutez un nouvel objet **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** ou **[Property](property-object-dao.md)** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ee7af-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

