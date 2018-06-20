---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782221"
---
# <a name="xleventregister"></a><span data-ttu-id="cc823-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="cc823-103">xlEventRegister</span></span>

 <span data-ttu-id="cc823-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cc823-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cc823-105">Utilisé pour enregistrer un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="cc823-105">Used to register an event handler.</span></span> <span data-ttu-id="cc823-106">Une nouveauté dans Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="cc823-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="cc823-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc823-107">Parameters</span></span>

 <span data-ttu-id="cc823-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="cc823-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="cc823-109">Le nom de la fonction de gestionnaire d’événements tel qu’il apparaît dans le code de la DLL.</span><span class="sxs-lookup"><span data-stu-id="cc823-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="cc823-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="cc823-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="cc823-111">L’événement est géré par la fonction désignée dans le paramètre _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="cc823-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="cc823-112">À compter d’Excel 2010, Excel prend en charge les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="cc823-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="cc823-113">**Événement**</span><span class="sxs-lookup"><span data-stu-id="cc823-113">**Event**</span></span>|<span data-ttu-id="cc823-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc823-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc823-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="cc823-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="cc823-116">Déclenché lorsque Excel termine un calcul.</span><span class="sxs-lookup"><span data-stu-id="cc823-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="cc823-117">Vous pouvez libérer les ressources allouées au cours du calcul après cet événement.</span><span class="sxs-lookup"><span data-stu-id="cc823-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="cc823-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="cc823-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="cc823-119">Déclenché lorsque l’utilisateur interrompt le calcul.</span><span class="sxs-lookup"><span data-stu-id="cc823-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="cc823-120">La ressource XLL doit s’arrêter toutes les activités asynchrones.</span><span class="sxs-lookup"><span data-stu-id="cc823-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="cc823-121">L’événement CalculationEnded est déclenché immédiatement après cet événement.</span><span class="sxs-lookup"><span data-stu-id="cc823-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="cc823-122">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cc823-122">Property value/Return value</span></span>

<span data-ttu-id="cc823-123">Si l’opération réussit, renvoie **la valeur TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="cc823-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="cc823-124">En cas d’échec, renvoie **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="cc823-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cc823-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc823-125">See also</span></span>



[<span data-ttu-id="cc823-126">Fonctions asynchrones définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cc823-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

