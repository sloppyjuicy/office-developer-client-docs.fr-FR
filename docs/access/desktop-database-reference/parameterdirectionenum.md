---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3da089a1369905b78d1a0724990afc22eb1d0dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470003"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="ae173-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="ae173-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="ae173-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae173-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ae173-104">Précise si le [paramètre](parameter-object-ado.md) représente un paramètre de saisie, de sortie, les deux à la fois, ou la valeur renvoyée par une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="ae173-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae173-105">Constant</span><span class="sxs-lookup"><span data-stu-id="ae173-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ae173-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae173-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ae173-107">Description</span><span class="sxs-lookup"><span data-stu-id="ae173-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae173-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="ae173-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="ae173-109">1</span><span class="sxs-lookup"><span data-stu-id="ae173-109">1</span></span></p></td>
<td><p><span data-ttu-id="ae173-p101">Par défaut. Indique que le paramètre est un paramètre de saisie.</span><span class="sxs-lookup"><span data-stu-id="ae173-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae173-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="ae173-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="ae173-113">3</span><span class="sxs-lookup"><span data-stu-id="ae173-113">3</span></span></p></td>
<td><p><span data-ttu-id="ae173-114">Indique que le paramètre est un paramètre de saisie et de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae173-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae173-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="ae173-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="ae173-116">2</span><span class="sxs-lookup"><span data-stu-id="ae173-116">2</span></span></p></td>
<td><p><span data-ttu-id="ae173-117">Indique que le paramètre représente un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae173-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae173-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="ae173-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="ae173-119">4</span><span class="sxs-lookup"><span data-stu-id="ae173-119">4</span></span></p></td>
<td><p><span data-ttu-id="ae173-120">Indique que le paramètre représente une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ae173-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae173-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="ae173-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="ae173-122">0</span><span class="sxs-lookup"><span data-stu-id="ae173-122">0</span></span></p></td>
<td><p><span data-ttu-id="ae173-123">Indique que la direction du paramètre est inconnue.</span><span class="sxs-lookup"><span data-stu-id="ae173-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae173-124">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="ae173-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="ae173-125">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ae173-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae173-126">Constante</span><span class="sxs-lookup"><span data-stu-id="ae173-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae173-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="ae173-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae173-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae173-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae173-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae173-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae173-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="ae173-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae173-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="ae173-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

