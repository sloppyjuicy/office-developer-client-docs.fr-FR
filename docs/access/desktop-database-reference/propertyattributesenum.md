---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717264"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="4bd9a-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="4bd9a-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="4bd9a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bd9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bd9a-104">Spécifie les attributs d'un objet [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4bd9a-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bd9a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="4bd9a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4bd9a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bd9a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4bd9a-107">Description</span><span class="sxs-lookup"><span data-stu-id="4bd9a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bd9a-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="4bd9a-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd9a-109">0</span><span class="sxs-lookup"><span data-stu-id="4bd9a-109">0</span></span></p></td>
<td><p><span data-ttu-id="4bd9a-110">Indique que la propriété n’est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4bd9a-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd9a-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="4bd9a-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd9a-112">1</span><span class="sxs-lookup"><span data-stu-id="4bd9a-112">1</span></span></p></td>
<td><p><span data-ttu-id="4bd9a-113">Indique que l'utilisateur doit spécifier une valeur pour cette propriété avant d'initialiser la source de données.</span><span class="sxs-lookup"><span data-stu-id="4bd9a-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd9a-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="4bd9a-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd9a-115">2</span><span class="sxs-lookup"><span data-stu-id="4bd9a-115">2</span></span></p></td>
<td><p><span data-ttu-id="4bd9a-116">Indique que l'utilisateur n'a pas besoin de spécifier une valeur pour cette propriété avant d'initialiser la source de données.</span><span class="sxs-lookup"><span data-stu-id="4bd9a-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd9a-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="4bd9a-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd9a-118">512</span><span class="sxs-lookup"><span data-stu-id="4bd9a-118">512</span></span></p></td>
<td><p><span data-ttu-id="4bd9a-119">Indique que l'utilisateur peut lire la propriété.</span><span class="sxs-lookup"><span data-stu-id="4bd9a-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd9a-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="4bd9a-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd9a-121">1024</span><span class="sxs-lookup"><span data-stu-id="4bd9a-121">1024</span></span></p></td>
<td><p><span data-ttu-id="4bd9a-122">Indique que l'utilisateur peut définir la propriété.</span><span class="sxs-lookup"><span data-stu-id="4bd9a-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4bd9a-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4bd9a-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="4bd9a-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4bd9a-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bd9a-125">Constante</span><span class="sxs-lookup"><span data-stu-id="4bd9a-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bd9a-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4bd9a-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd9a-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="4bd9a-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd9a-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="4bd9a-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd9a-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="4bd9a-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd9a-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="4bd9a-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

