---
title: PersistFormatEnum (référence de base de données du bureau Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a1e980debebe6a38ed0c27eabba3abefcd8be152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887151"
---
# <a name="persistformatenum"></a><span data-ttu-id="990de-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="990de-102">PersistFormatEnum</span></span>

<span data-ttu-id="990de-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="990de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="990de-104">Spécifie le format dans lequel enregistrer un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="990de-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="990de-105">Constant</span><span class="sxs-lookup"><span data-stu-id="990de-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="990de-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="990de-106">Value</span></span></p></th>
<th><p><span data-ttu-id="990de-107">Description</span><span class="sxs-lookup"><span data-stu-id="990de-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="990de-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="990de-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="990de-109">0</span><span class="sxs-lookup"><span data-stu-id="990de-109">0</span></span></p></td>
<td><p><span data-ttu-id="990de-110">Indique le format Advanced Data TableGram (ADTG) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="990de-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="990de-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="990de-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="990de-112">1</span><span class="sxs-lookup"><span data-stu-id="990de-112">1</span></span></p></td>
<td><p><span data-ttu-id="990de-p101">Indique que le format XML (Extensible Markup Language) propre à ADO sera utilisé. Cette valeur est identique à adPersistXML et autorise la compatibilité ascendante.</span><span class="sxs-lookup"><span data-stu-id="990de-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="990de-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="990de-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="990de-116">1</span><span class="sxs-lookup"><span data-stu-id="990de-116">1</span></span></p></td>
<td><p><span data-ttu-id="990de-117">Indique le format XML (Extensible Markup Language).</span><span class="sxs-lookup"><span data-stu-id="990de-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="990de-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="990de-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="990de-119">2</span><span class="sxs-lookup"><span data-stu-id="990de-119">2</span></span></p></td>
<td><p><span data-ttu-id="990de-120">Indique que le fournisseur maintient <strong>Recordset</strong> à l'aide de son propre format.</span><span class="sxs-lookup"><span data-stu-id="990de-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="990de-121">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="990de-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="990de-122">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="990de-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="990de-123">Constante</span><span class="sxs-lookup"><span data-stu-id="990de-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="990de-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="990de-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="990de-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="990de-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

