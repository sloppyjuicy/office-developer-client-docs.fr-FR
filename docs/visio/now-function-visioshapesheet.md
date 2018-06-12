---
title: Maintenant fonction (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Renvoie la valeur de date et l’heure actuelle.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789200"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="d1955-103">Maintenant fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d1955-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d1955-104">Renvoie la valeur de date et l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="d1955-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d1955-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1955-105">Syntax</span></span>

<span data-ttu-id="d1955-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="d1955-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="d1955-107">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d1955-107">Return value</span></span>

<span data-ttu-id="d1955-108">Datetime</span><span class="sxs-lookup"><span data-stu-id="d1955-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1955-109">Note</span><span class="sxs-lookup"><span data-stu-id="d1955-109">Remarks</span></span>

<span data-ttu-id="d1955-110">La fonction NOW est automatiquement recalculée toutes les minutes.</span><span class="sxs-lookup"><span data-stu-id="d1955-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d1955-111">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="d1955-111">Example 1</span></span>

<span data-ttu-id="d1955-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="d1955-112">NOW( )</span></span>
  
<span data-ttu-id="d1955-113">Renvoie la date et l’heure actuelles, 27/09/10 12:03:30, par exemple.</span><span class="sxs-lookup"><span data-stu-id="d1955-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d1955-114">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="d1955-114">Example 2</span></span>

<span data-ttu-id="d1955-115">FORMAT(NOW(),"jj MMM. aaaa hh:mm")</span><span class="sxs-lookup"><span data-stu-id="d1955-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="d1955-116">Renvoie la date et l’heure actuelles au format 27 sept. 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="d1955-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d1955-117">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="d1955-117">Example 3</span></span>

<span data-ttu-id="d1955-118">NOW()+2WE.</span><span class="sxs-lookup"><span data-stu-id="d1955-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="d1955-119">Renvoie la date et l’heure actuelles plus deux semaines, soit 10/11/10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="d1955-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

