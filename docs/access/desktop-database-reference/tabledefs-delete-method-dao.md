---
title: Méthode TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709319"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="a29ae-102">Méthode TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="a29ae-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="a29ae-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a29ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a29ae-104">Supprime l'objet **TableDef** spécifié de la collection **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="a29ae-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a29ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a29ae-105">Syntax</span></span>

<span data-ttu-id="a29ae-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="a29ae-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="a29ae-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="a29ae-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a29ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a29ae-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a29ae-109">Nom</span><span class="sxs-lookup"><span data-stu-id="a29ae-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a29ae-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="a29ae-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a29ae-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a29ae-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a29ae-112">Description</span><span class="sxs-lookup"><span data-stu-id="a29ae-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a29ae-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="a29ae-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="a29ae-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a29ae-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a29ae-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a29ae-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a29ae-116">Nom de l'objet TableDef à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a29ae-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a29ae-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a29ae-117">Remarks</span></span>

<span data-ttu-id="a29ae-118">La méthode Delete est pris en charge uniquement lorsque l’objet **TableDef** est nouveau et n’a pas été ajouté à la base de données, ou lorsque la propriété **Updatable** de l' **objet TableDef** est définie sur **True**.</span><span class="sxs-lookup"><span data-stu-id="a29ae-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

