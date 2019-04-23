---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287971"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="23f2a-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="23f2a-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="23f2a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23f2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23f2a-104">Précise si le [paramètre](parameter-object-ado.md) représente un paramètre de saisie, de sortie, les deux à la fois, ou la valeur renvoyée par une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="23f2a-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23f2a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="23f2a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="23f2a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="23f2a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="23f2a-107">Description</span><span class="sxs-lookup"><span data-stu-id="23f2a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23f2a-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="23f2a-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="23f2a-109">0,1</span><span class="sxs-lookup"><span data-stu-id="23f2a-109">1</span></span></p></td>
<td><p><span data-ttu-id="23f2a-p101">Par défaut. Indique que le paramètre est un paramètre de saisie.</span><span class="sxs-lookup"><span data-stu-id="23f2a-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23f2a-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="23f2a-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="23f2a-113">3</span><span class="sxs-lookup"><span data-stu-id="23f2a-113">3</span></span></p></td>
<td><p><span data-ttu-id="23f2a-114">Indique que le paramètre est un paramètre de saisie et de sortie.</span><span class="sxs-lookup"><span data-stu-id="23f2a-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23f2a-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="23f2a-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="23f2a-116">n°2</span><span class="sxs-lookup"><span data-stu-id="23f2a-116">2</span></span></p></td>
<td><p><span data-ttu-id="23f2a-117">Indique que le paramètre représente un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="23f2a-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23f2a-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="23f2a-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="23f2a-119">4</span><span class="sxs-lookup"><span data-stu-id="23f2a-119">4</span></span></p></td>
<td><p><span data-ttu-id="23f2a-120">Indique que le paramètre représente une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="23f2a-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23f2a-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="23f2a-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="23f2a-122">0</span><span class="sxs-lookup"><span data-stu-id="23f2a-122">0</span></span></p></td>
<td><p><span data-ttu-id="23f2a-123">Indique que la direction du paramètre est inconnue.</span><span class="sxs-lookup"><span data-stu-id="23f2a-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="23f2a-124">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="23f2a-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="23f2a-125">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="23f2a-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23f2a-126">Constante</span><span class="sxs-lookup"><span data-stu-id="23f2a-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23f2a-127">AdoEnums. ParameterDirection. INPUT</span><span class="sxs-lookup"><span data-stu-id="23f2a-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23f2a-128">AdoEnums. ParameterDirection. INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="23f2a-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23f2a-129">AdoEnums. ParameterDirection. OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23f2a-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23f2a-130">AdoEnums. ParameterDirection. RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="23f2a-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23f2a-131">AdoEnums. ParameterDirection. unKNOWn</span><span class="sxs-lookup"><span data-stu-id="23f2a-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

