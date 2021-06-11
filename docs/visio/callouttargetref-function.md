---
title: CALLOUTTARGETREF, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Renvoie une référence de feuille à la forme cible de la forme de légende.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423012"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="54efa-103">Fonction CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="54efa-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="54efa-104">Renvoie une référence de feuille à la forme cible de la forme de légende.</span><span class="sxs-lookup"><span data-stu-id="54efa-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="54efa-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="54efa-105">Version Information</span></span>

<span data-ttu-id="54efa-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="54efa-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="54efa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54efa-107">Syntax</span></span>

<span data-ttu-id="54efa-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="54efa-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="54efa-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54efa-109">Return value</span></span>

<span data-ttu-id="54efa-110">Référence ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="54efa-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54efa-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="54efa-111">Remarks</span></span>

<span data-ttu-id="54efa-112">Si la forme n’est pas une forme de fin ou si elle n’est pas associée à une forme cible, callOUTTARGETREF renvoie #REF.</span><span class="sxs-lookup"><span data-stu-id="54efa-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="54efa-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="54efa-113">Example</span></span>

<span data-ttu-id="54efa-114">CALLOUTTARGETREF()! Height</span><span class="sxs-lookup"><span data-stu-id="54efa-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="54efa-115">Renvoie la valeur de la cellule Height de la forme associée à la légende.</span><span class="sxs-lookup"><span data-stu-id="54efa-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

