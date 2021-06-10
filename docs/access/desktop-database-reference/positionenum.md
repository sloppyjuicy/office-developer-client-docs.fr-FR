---
title: PositionEnum (référence de base de données de bureau Access)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287502"
---
# <a name="positionenum"></a><span data-ttu-id="37a67-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="37a67-102">PositionEnum</span></span>

<span data-ttu-id="37a67-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37a67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37a67-104">Spécifie la position en cours du pointeur de l’enregistrement dans un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37a67-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37a67-105">Constante</span><span class="sxs-lookup"><span data-stu-id="37a67-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="37a67-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="37a67-106">Value</span></span></p></th>
<th><p><span data-ttu-id="37a67-107">Description</span><span class="sxs-lookup"><span data-stu-id="37a67-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37a67-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="37a67-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="37a67-109">-2</span><span class="sxs-lookup"><span data-stu-id="37a67-109">-2</span></span></p></td>
<td><p><span data-ttu-id="37a67-110">Indique que le pointeur de l’enregistrement en cours est de type BOF (la propriété <a href="bof-eof-properties-ado.md">BOF</a> est <strong>True</strong>).</span><span class="sxs-lookup"><span data-stu-id="37a67-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37a67-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="37a67-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="37a67-112">-3</span><span class="sxs-lookup"><span data-stu-id="37a67-112">-3</span></span></p></td>
<td><p><span data-ttu-id="37a67-113">Indique que le pointeur de l’enregistrement en cours est de type EOF (la propriété <a href="bof-eof-properties-ado.md">EOF</a> est <strong>True</strong>).</span><span class="sxs-lookup"><span data-stu-id="37a67-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37a67-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="37a67-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="37a67-115">-1</span><span class="sxs-lookup"><span data-stu-id="37a67-115">-1</span></span></p></td>
<td><p><span data-ttu-id="37a67-116">Indique que l’objet <strong>Recordset</strong> est vide, que la position en cours n’est pas connue, ou que le fournisseur ne prend pas en charge la propriété <a href="absolutepage-property-ado.md">AbsolutePage</a> ou <a href="absoluteposition-property-ado.md">AbsolutePosition</a>.</span><span class="sxs-lookup"><span data-stu-id="37a67-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="37a67-117">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="37a67-117">ADO/WFC equivalent</span></span>

<span data-ttu-id="37a67-118">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="37a67-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37a67-119">Constante</span><span class="sxs-lookup"><span data-stu-id="37a67-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37a67-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="37a67-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37a67-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="37a67-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37a67-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="37a67-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

