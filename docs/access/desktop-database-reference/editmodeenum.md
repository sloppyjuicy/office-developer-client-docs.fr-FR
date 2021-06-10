---
title: EditModeEnum (référence de base de données de bureau Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293580"
---
# <a name="editmodeenum"></a><span data-ttu-id="2b04d-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="2b04d-102">EditModeEnum</span></span>

<span data-ttu-id="2b04d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b04d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b04d-104">Spécifie l'état d'édition d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2b04d-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b04d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="2b04d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2b04d-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b04d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2b04d-107">Description</span><span class="sxs-lookup"><span data-stu-id="2b04d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b04d-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="2b04d-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="2b04d-109">0</span><span class="sxs-lookup"><span data-stu-id="2b04d-109">0</span></span></p></td>
<td><p><span data-ttu-id="2b04d-110">Indique qu'aucune opération d'édition n'est en cours.</span><span class="sxs-lookup"><span data-stu-id="2b04d-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b04d-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="2b04d-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="2b04d-112">1</span><span class="sxs-lookup"><span data-stu-id="2b04d-112">1</span></span></p></td>
<td><p><span data-ttu-id="2b04d-113">Indique que les données de l'enregistrement en cours ont été modifiées, mais pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="2b04d-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b04d-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="2b04d-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="2b04d-115">2</span><span class="sxs-lookup"><span data-stu-id="2b04d-115">2</span></span></p></td>
<td><p><span data-ttu-id="2b04d-116">Indique que la méthode <a href="addnew-method-ado.md">AddNew</a> a été appelée et que l’enregistrement en cours dans la zone tampon de copie est un nouvel enregistrement qui n’a pas été enregistré dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="2b04d-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b04d-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="2b04d-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="2b04d-118">4 </span><span class="sxs-lookup"><span data-stu-id="2b04d-118">4</span></span></p></td>
<td><p><span data-ttu-id="2b04d-119">Indique que l'enregistrement en cours a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="2b04d-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2b04d-120">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2b04d-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="2b04d-121">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2b04d-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b04d-122">Constante</span><span class="sxs-lookup"><span data-stu-id="2b04d-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b04d-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="2b04d-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b04d-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="2b04d-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b04d-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="2b04d-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b04d-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="2b04d-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

