---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160278"
---
# <a name="xleventregister"></a><span data-ttu-id="c0936-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="c0936-103">xlEventRegister</span></span>

 <span data-ttu-id="c0936-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0936-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0936-105">Utilisé pour inscrire un handler d’événements.</span><span class="sxs-lookup"><span data-stu-id="c0936-105">Used to register an event handler.</span></span> <span data-ttu-id="c0936-106">Introduit dans Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="c0936-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="c0936-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0936-107">Parameters</span></span>

 <span data-ttu-id="c0936-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="c0936-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="c0936-109">Nom de la fonction de handler d’événement telle qu’elle apparaît dans le code DLL.</span><span class="sxs-lookup"><span data-stu-id="c0936-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="c0936-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="c0936-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="c0936-111">Événement géré par la fonction désignée dans le _paramètre pxProcedure._</span><span class="sxs-lookup"><span data-stu-id="c0936-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="c0936-112">À compter d’Excel 2010, Excel prend en charge les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="c0936-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="c0936-113">**Événement**</span><span class="sxs-lookup"><span data-stu-id="c0936-113">**Event**</span></span>|<span data-ttu-id="c0936-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0936-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0936-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="c0936-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="c0936-116">Élevé lorsque Excel termine un calcul.</span><span class="sxs-lookup"><span data-stu-id="c0936-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="c0936-117">Vous pouvez libérer toutes les ressources allouées pendant le calcul après cet événement.</span><span class="sxs-lookup"><span data-stu-id="c0936-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="c0936-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="c0936-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="c0936-119">Élevé lorsque l’utilisateur interrompt le calcul.</span><span class="sxs-lookup"><span data-stu-id="c0936-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="c0936-120">Le XLL doit arrêter toutes les activités asynchrones.</span><span class="sxs-lookup"><span data-stu-id="c0936-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="c0936-121">L’événement CalculationEnded est lancé immédiatement après cet événement.</span><span class="sxs-lookup"><span data-stu-id="c0936-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="c0936-122">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="c0936-122">Property value/Return value</span></span>

<span data-ttu-id="c0936-123">Si elle réussit, pxRes (**xltypeInt**) a une valeur > 0.</span><span class="sxs-lookup"><span data-stu-id="c0936-123">If successful, pxRes (**xltypeInt**) has a value > 0.</span></span> <span data-ttu-id="c0936-124">En cas d’échec, pxRes ==0.</span><span class="sxs-lookup"><span data-stu-id="c0936-124">If unsuccessful, pxRes ==0.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0936-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0936-125">See also</span></span>



[<span data-ttu-id="c0936-126">Fonctions asynchrones définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c0936-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

