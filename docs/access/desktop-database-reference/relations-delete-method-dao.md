---
title: Méthode Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998923"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="66552-102">Méthode Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="66552-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="66552-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66552-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66552-104">Supprime l'objet **Relation** spécifié de la collection **Relations**.</span><span class="sxs-lookup"><span data-stu-id="66552-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="66552-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66552-105">Syntax</span></span>

<span data-ttu-id="66552-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="66552-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="66552-107">*expression* Variable qui représente un objet **Relations** .</span><span class="sxs-lookup"><span data-stu-id="66552-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="66552-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66552-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66552-109">Name</span><span class="sxs-lookup"><span data-stu-id="66552-109">Name</span></span></p></th>
<th><p><span data-ttu-id="66552-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="66552-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="66552-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="66552-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="66552-112">Description</span><span class="sxs-lookup"><span data-stu-id="66552-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66552-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="66552-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="66552-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66552-114">Required</span></span></p></td>
<td><p><span data-ttu-id="66552-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="66552-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="66552-116">Nom de la relation à supprimer.</span><span class="sxs-lookup"><span data-stu-id="66552-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="66552-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="66552-117">Remarks</span></span>

<span data-ttu-id="66552-118">La méthode **Delete** n'est prise en charge que lorsque l'objet **Relation** est un nouvel objet qui n'a pas été ajouté.</span><span class="sxs-lookup"><span data-stu-id="66552-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

