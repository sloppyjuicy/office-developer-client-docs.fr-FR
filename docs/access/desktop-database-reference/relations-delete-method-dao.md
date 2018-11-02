---
title: Méthode Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462581e5b1ab3f09b697ee7f4b763a889d8119fd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925526"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="1060f-102">Méthode Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="1060f-102">Relations.Delete method (DAO)</span></span>


<span data-ttu-id="1060f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1060f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1060f-104">Supprime l'objet **Relation** spécifié de la collection **Relations**.</span><span class="sxs-lookup"><span data-stu-id="1060f-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1060f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1060f-105">Syntax</span></span>

<span data-ttu-id="1060f-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="1060f-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="1060f-107">*expression* Variable qui représente un objet **Relations** .</span><span class="sxs-lookup"><span data-stu-id="1060f-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1060f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1060f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1060f-109">Name</span><span class="sxs-lookup"><span data-stu-id="1060f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1060f-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="1060f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1060f-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="1060f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1060f-112">Description</span><span class="sxs-lookup"><span data-stu-id="1060f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1060f-113">Name</span><span class="sxs-lookup"><span data-stu-id="1060f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="1060f-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1060f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1060f-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="1060f-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1060f-116">Nom de la relation à supprimer.</span><span class="sxs-lookup"><span data-stu-id="1060f-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1060f-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="1060f-117">Remarks</span></span>

<span data-ttu-id="1060f-118">La méthode **Delete** n'est prise en charge que lorsque l'objet **Relation** est un nouvel objet qui n'a pas été ajouté.</span><span class="sxs-lookup"><span data-stu-id="1060f-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

