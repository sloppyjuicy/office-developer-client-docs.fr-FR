---
title: NOW Function (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Renvoie la date et l’heure actuelles.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414080"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="67a59-103">NOW Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="67a59-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="67a59-104">Renvoie la date et l’heure actuelles.</span><span class="sxs-lookup"><span data-stu-id="67a59-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="67a59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67a59-105">Syntax</span></span>

<span data-ttu-id="67a59-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="67a59-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="67a59-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67a59-107">Return value</span></span>

<span data-ttu-id="67a59-108">Datetime</span><span class="sxs-lookup"><span data-stu-id="67a59-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67a59-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="67a59-109">Remarks</span></span>

<span data-ttu-id="67a59-110">La fonction NOW est automatiquement recalculée toutes les minutes.</span><span class="sxs-lookup"><span data-stu-id="67a59-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="67a59-111">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="67a59-111">Example 1</span></span>

<span data-ttu-id="67a59-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="67a59-112">NOW( )</span></span>
  
<span data-ttu-id="67a59-113">Renvoie la date et l’heure actuelles, 27/09/10 12:03:30, par exemple.</span><span class="sxs-lookup"><span data-stu-id="67a59-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="67a59-114">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="67a59-114">Example 2</span></span>

<span data-ttu-id="67a59-115">FORMAT(NOW(),"jj MMM. aaaa hh:mm")</span><span class="sxs-lookup"><span data-stu-id="67a59-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="67a59-116">Renvoie la date et l’heure actuelles au format 27 sept. 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="67a59-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="67a59-117">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="67a59-117">Example 3</span></span>

<span data-ttu-id="67a59-118">NOW()+2EW.</span><span class="sxs-lookup"><span data-stu-id="67a59-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="67a59-119">Renvoie la date et l’heure actuelles plus deux semaines, soit 10/11/10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="67a59-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

