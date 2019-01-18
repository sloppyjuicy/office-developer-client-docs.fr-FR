---
title: Méthode Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716431"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="41018-102">Méthode Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="41018-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="41018-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41018-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41018-104">Supprime l'objet **Relation** spécifié de la collection **Relations**.</span><span class="sxs-lookup"><span data-stu-id="41018-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="41018-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41018-105">Syntax</span></span>

<span data-ttu-id="41018-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="41018-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="41018-107">*expression* Variable qui représente un objet **Relations** .</span><span class="sxs-lookup"><span data-stu-id="41018-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="41018-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41018-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41018-109">Nom</span><span class="sxs-lookup"><span data-stu-id="41018-109">Name</span></span></p></th>
<th><p><span data-ttu-id="41018-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="41018-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="41018-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="41018-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="41018-112">Description</span><span class="sxs-lookup"><span data-stu-id="41018-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41018-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="41018-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="41018-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="41018-114">Required</span></span></p></td>
<td><p><span data-ttu-id="41018-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="41018-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="41018-116">Nom de la relation à supprimer.</span><span class="sxs-lookup"><span data-stu-id="41018-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="41018-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="41018-117">Remarks</span></span>

<span data-ttu-id="41018-118">La méthode **Delete** n'est prise en charge que lorsque l'objet **Relation** est un nouvel objet qui n'a pas été ajouté.</span><span class="sxs-lookup"><span data-stu-id="41018-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

