---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438763"
---
# <a name="xleventregister"></a><span data-ttu-id="b362b-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="b362b-103">xlEventRegister</span></span>

 <span data-ttu-id="b362b-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b362b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b362b-105">Permet d'enregistrer un gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="b362b-105">Used to register an event handler.</span></span> <span data-ttu-id="b362b-106">Introduit dans Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="b362b-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="b362b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b362b-107">Parameters</span></span>

 <span data-ttu-id="b362b-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b362b-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b362b-109">Nom de la fonction de gestionnaire d'événements telle qu'elle apparaît dans le code de la DLL.</span><span class="sxs-lookup"><span data-stu-id="b362b-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="b362b-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="b362b-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="b362b-111">Événement géré par la fonction désignée dans le paramètre _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="b362b-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="b362b-112">À partir d'Excel 2010, Excel prend en charge les événements suivants:</span><span class="sxs-lookup"><span data-stu-id="b362b-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="b362b-113">**event**</span><span class="sxs-lookup"><span data-stu-id="b362b-113">**Event**</span></span>|<span data-ttu-id="b362b-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="b362b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b362b-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="b362b-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="b362b-116">Déclenché lorsqu'Excel termine un calcul.</span><span class="sxs-lookup"><span data-stu-id="b362b-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="b362b-117">Vous pouvez libérer toutes les ressources allouées pendant le calcul après cet événement.</span><span class="sxs-lookup"><span data-stu-id="b362b-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="b362b-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="b362b-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="b362b-119">Déclenché lorsque l'utilisateur interrompt le calcul.</span><span class="sxs-lookup"><span data-stu-id="b362b-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="b362b-120">Le XLL doit arrêter les activités asynchrones.</span><span class="sxs-lookup"><span data-stu-id="b362b-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="b362b-121">L'événement CalculationEnded est déclenché immédiatement après cet événement.</span><span class="sxs-lookup"><span data-stu-id="b362b-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="b362b-122">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="b362b-122">Property value/Return value</span></span>

<span data-ttu-id="b362b-123">Si elle réussit, renvoie la **valeur true** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="b362b-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="b362b-124">En cas d'échec, renvoie **false**.</span><span class="sxs-lookup"><span data-stu-id="b362b-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b362b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b362b-125">See also</span></span>



[<span data-ttu-id="b362b-126">Fonctions asynchrones définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b362b-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

