---
title: CALLOUTTARGETREF, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Renvoie une référence de feuille à la forme cible de la forme de légende.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788173"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="b46ec-103">CALLOUTTARGETREF, fonction</span><span class="sxs-lookup"><span data-stu-id="b46ec-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="b46ec-104">Renvoie une référence de feuille à la forme cible de la forme de légende.</span><span class="sxs-lookup"><span data-stu-id="b46ec-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="b46ec-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="b46ec-105">Version Information</span></span>

<span data-ttu-id="b46ec-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="b46ec-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b46ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b46ec-107">Syntax</span></span>

<span data-ttu-id="b46ec-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="b46ec-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="b46ec-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b46ec-109">Return value</span></span>

<span data-ttu-id="b46ec-110">Référence ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="b46ec-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b46ec-111">Note</span><span class="sxs-lookup"><span data-stu-id="b46ec-111">Remarks</span></span>

<span data-ttu-id="b46ec-112">Si la forme n’est pas une forme de légende, ou si elle n’est pas associé à une forme cible, CALLOUTTARGETREF renvoie #REF.</span><span class="sxs-lookup"><span data-stu-id="b46ec-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="b46ec-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="b46ec-113">Example</span></span>

<span data-ttu-id="b46ec-114">CALLOUTTARGETREF()!Height</span><span class="sxs-lookup"><span data-stu-id="b46ec-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="b46ec-115">Renvoie la valeur de la cellule Height de la forme associée à la légende.</span><span class="sxs-lookup"><span data-stu-id="b46ec-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

