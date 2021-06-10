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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302876"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="faa3e-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="faa3e-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="faa3e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="faa3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="faa3e-104">Spécifie les attributs d’un objet [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="faa3e-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="faa3e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="faa3e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="faa3e-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="faa3e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="faa3e-107">Description</span><span class="sxs-lookup"><span data-stu-id="faa3e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa3e-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="faa3e-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="faa3e-109">0</span><span class="sxs-lookup"><span data-stu-id="faa3e-109">0</span></span></p></td>
<td><p><span data-ttu-id="faa3e-110">Indique que la propriété n’est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="faa3e-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa3e-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="faa3e-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="faa3e-112">1</span><span class="sxs-lookup"><span data-stu-id="faa3e-112">1</span></span></p></td>
<td><p><span data-ttu-id="faa3e-113">Indique que l'utilisateur doit spécifier une valeur pour cette propriété avant d'initialiser la source de données.</span><span class="sxs-lookup"><span data-stu-id="faa3e-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa3e-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="faa3e-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="faa3e-115">2</span><span class="sxs-lookup"><span data-stu-id="faa3e-115">2</span></span></p></td>
<td><p><span data-ttu-id="faa3e-116">Indique que l'utilisateur n'a pas besoin de spécifier une valeur pour cette propriété avant d'initialiser la source de données.</span><span class="sxs-lookup"><span data-stu-id="faa3e-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa3e-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="faa3e-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="faa3e-118">512</span><span class="sxs-lookup"><span data-stu-id="faa3e-118">512</span></span></p></td>
<td><p><span data-ttu-id="faa3e-119">Indique que l'utilisateur peut lire la propriété.</span><span class="sxs-lookup"><span data-stu-id="faa3e-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa3e-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="faa3e-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="faa3e-121">1024</span><span class="sxs-lookup"><span data-stu-id="faa3e-121">1024</span></span></p></td>
<td><p><span data-ttu-id="faa3e-122">Indique que l'utilisateur peut définir la propriété.</span><span class="sxs-lookup"><span data-stu-id="faa3e-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="faa3e-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="faa3e-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="faa3e-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="faa3e-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="faa3e-125">Constante</span><span class="sxs-lookup"><span data-stu-id="faa3e-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa3e-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="faa3e-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa3e-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="faa3e-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa3e-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="faa3e-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa3e-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="faa3e-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa3e-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="faa3e-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

