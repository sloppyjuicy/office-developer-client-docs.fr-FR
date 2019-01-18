---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f9fdf9dd5908b65ae3b6f6ce5a44eba07e4d9bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709858"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="48d3c-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="48d3c-102">SearchDirectionEnum</span></span>


<span data-ttu-id="48d3c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48d3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48d3c-104">Spécifie le sens d'une recherche d'enregistrement dans un [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="48d3c-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48d3c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="48d3c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="48d3c-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="48d3c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="48d3c-107">Description</span><span class="sxs-lookup"><span data-stu-id="48d3c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48d3c-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="48d3c-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="48d3c-109">-1</span><span class="sxs-lookup"><span data-stu-id="48d3c-109">-1</span></span></p></td>
<td><p><span data-ttu-id="48d3c-p101">Recherche vers le début, en s’arrêtant en haut du <strong>Recordset</strong>. Si aucune correspondance n’est trouvée, le pointeur de l’enregistrement est placé sur <a href="bof-eof-properties-ado.md">BOF</a>.</span><span class="sxs-lookup"><span data-stu-id="48d3c-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48d3c-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="48d3c-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="48d3c-113">1</span><span class="sxs-lookup"><span data-stu-id="48d3c-113">1</span></span></p></td>
<td><p><span data-ttu-id="48d3c-p102">Recherche vers la fin, en s’arrêtant en bas du <strong>Recordset</strong>. Si aucune correspondance n’est trouvée, le pointeur de l’enregistrement est placé sur <a href="bof-eof-properties-ado.md">EOF</a>.</span><span class="sxs-lookup"><span data-stu-id="48d3c-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="48d3c-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="48d3c-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="48d3c-117">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="48d3c-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48d3c-118">Constante</span><span class="sxs-lookup"><span data-stu-id="48d3c-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48d3c-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="48d3c-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48d3c-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="48d3c-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

