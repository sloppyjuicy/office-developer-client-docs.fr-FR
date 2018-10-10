---
title: EditModeEnum (référence de base de données du bureau Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7322193971e4230afaacbb1f614c7ab682f3c149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471001"
---
# <a name="editmodeenum"></a><span data-ttu-id="c73c4-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="c73c4-102">EditModeEnum</span></span>


<span data-ttu-id="c73c4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c73c4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c73c4-104">Spécifie l'état d'édition d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c73c4-104">Specifies the editing status of a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c73c4-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c73c4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c73c4-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="c73c4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c73c4-107">Description</span><span class="sxs-lookup"><span data-stu-id="c73c4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c73c4-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="c73c4-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="c73c4-109">0</span><span class="sxs-lookup"><span data-stu-id="c73c4-109">0</span></span></p></td>
<td><p><span data-ttu-id="c73c4-110">Indique qu'aucune opération d'édition n'est en cours.</span><span class="sxs-lookup"><span data-stu-id="c73c4-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73c4-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="c73c4-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="c73c4-112">1</span><span class="sxs-lookup"><span data-stu-id="c73c4-112">1</span></span></p></td>
<td><p><span data-ttu-id="c73c4-113">Indique que les données de l'enregistrement en cours ont été modifiées, mais pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c73c4-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73c4-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="c73c4-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="c73c4-115">2</span><span class="sxs-lookup"><span data-stu-id="c73c4-115">2</span></span></p></td>
<td><p><span data-ttu-id="c73c4-116">Indique que la méthode <a href="addnew-method-ado.md">AddNew</a> a été appelée et que l’enregistrement en cours dans la zone tampon de copie est un nouvel enregistrement qui n’a pas été enregistré dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="c73c4-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73c4-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="c73c4-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="c73c4-118">4</span><span class="sxs-lookup"><span data-stu-id="c73c4-118">4</span></span></p></td>
<td><p><span data-ttu-id="c73c4-119">Indique que l'enregistrement en cours a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c73c4-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c73c4-120">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="c73c4-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c73c4-121">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c73c4-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c73c4-122">Constante</span><span class="sxs-lookup"><span data-stu-id="c73c4-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c73c4-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="c73c4-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73c4-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="c73c4-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73c4-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="c73c4-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73c4-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="c73c4-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

