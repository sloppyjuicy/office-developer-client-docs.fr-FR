---
title: PersistFormatEnum (référence de base de données du bureau Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4954c09c3eff67bb6f55dfc9e49464ad58fad5e6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718090"
---
# <a name="persistformatenum"></a><span data-ttu-id="dc5a1-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="dc5a1-102">PersistFormatEnum</span></span>

<span data-ttu-id="dc5a1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc5a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc5a1-104">Spécifie le format dans lequel enregistrer un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dc5a1-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc5a1-105">Constante</span><span class="sxs-lookup"><span data-stu-id="dc5a1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="dc5a1-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc5a1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dc5a1-107">Description</span><span class="sxs-lookup"><span data-stu-id="dc5a1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc5a1-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="dc5a1-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5a1-109">0</span><span class="sxs-lookup"><span data-stu-id="dc5a1-109">0</span></span></p></td>
<td><p><span data-ttu-id="dc5a1-110">Indique le format Advanced Data TableGram (ADTG) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc5a1-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc5a1-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="dc5a1-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5a1-112">1</span><span class="sxs-lookup"><span data-stu-id="dc5a1-112">1</span></span></p></td>
<td><p><span data-ttu-id="dc5a1-p101">Indique que le format XML (Extensible Markup Language) propre à ADO sera utilisé. Cette valeur est identique à adPersistXML et autorise la compatibilité ascendante.</span><span class="sxs-lookup"><span data-stu-id="dc5a1-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc5a1-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="dc5a1-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5a1-116">1</span><span class="sxs-lookup"><span data-stu-id="dc5a1-116">1</span></span></p></td>
<td><p><span data-ttu-id="dc5a1-117">Indique le format XML (Extensible Markup Language).</span><span class="sxs-lookup"><span data-stu-id="dc5a1-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc5a1-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="dc5a1-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5a1-119">2</span><span class="sxs-lookup"><span data-stu-id="dc5a1-119">2</span></span></p></td>
<td><p><span data-ttu-id="dc5a1-120">Indique que le fournisseur maintient <strong>Recordset</strong> à l'aide de son propre format.</span><span class="sxs-lookup"><span data-stu-id="dc5a1-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="dc5a1-121">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="dc5a1-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="dc5a1-122">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="dc5a1-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc5a1-123">Constante</span><span class="sxs-lookup"><span data-stu-id="dc5a1-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc5a1-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="dc5a1-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc5a1-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="dc5a1-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

