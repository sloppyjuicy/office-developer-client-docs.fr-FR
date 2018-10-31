---
title: EditModeEnum (référence de base de données du bureau Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 790d28fa1efec5d5ad212094cb75f9d8d6456dbe
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860272"
---
# <a name="editmodeenum"></a><span data-ttu-id="09e4a-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="09e4a-102">EditModeEnum</span></span>

<span data-ttu-id="09e4a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="09e4a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="09e4a-104">Spécifie l'état d'édition d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="09e4a-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09e4a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="09e4a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="09e4a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e4a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="09e4a-107">Description</span><span class="sxs-lookup"><span data-stu-id="09e4a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09e4a-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="09e4a-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="09e4a-109">0</span><span class="sxs-lookup"><span data-stu-id="09e4a-109">0</span></span></p></td>
<td><p><span data-ttu-id="09e4a-110">Indique qu'aucune opération d'édition n'est en cours.</span><span class="sxs-lookup"><span data-stu-id="09e4a-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e4a-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="09e4a-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="09e4a-112">1</span><span class="sxs-lookup"><span data-stu-id="09e4a-112">1</span></span></p></td>
<td><p><span data-ttu-id="09e4a-113">Indique que les données de l'enregistrement en cours ont été modifiées, mais pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="09e4a-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09e4a-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="09e4a-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="09e4a-115">2</span><span class="sxs-lookup"><span data-stu-id="09e4a-115">2</span></span></p></td>
<td><p><span data-ttu-id="09e4a-116">Indique que la méthode <a href="addnew-method-ado.md">AddNew</a> a été appelée et que l’enregistrement en cours dans la zone tampon de copie est un nouvel enregistrement qui n’a pas été enregistré dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="09e4a-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e4a-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="09e4a-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="09e4a-118">4</span><span class="sxs-lookup"><span data-stu-id="09e4a-118">4</span></span></p></td>
<td><p><span data-ttu-id="09e4a-119">Indique que l'enregistrement en cours a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="09e4a-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="09e4a-120">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="09e4a-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="09e4a-121">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="09e4a-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09e4a-122">Constante</span><span class="sxs-lookup"><span data-stu-id="09e4a-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09e4a-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="09e4a-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e4a-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="09e4a-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09e4a-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="09e4a-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e4a-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="09e4a-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

