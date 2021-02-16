---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438266"
---
# <a name="handling-events"></a><span data-ttu-id="e38d6-103">Gestion d'événements</span><span class="sxs-lookup"><span data-stu-id="e38d6-103">Handling Events</span></span>

 <span data-ttu-id="e38d6-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e38d6-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e38d6-105">À partir d’Excel 2010, les XL peuvent recevoir des événements conçus pour gérer le cycle de vie de la fonction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e38d6-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="e38d6-106">Les événements sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e38d6-106">The events are as follows:</span></span>
  
- <span data-ttu-id="e38d6-107">**CalculationEnded :** élevé lorsque Excel a terminé le calcul.</span><span class="sxs-lookup"><span data-stu-id="e38d6-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="e38d6-108">Après cet événement, vous pouvez libérer les ressources allouées pendant le calcul.</span><span class="sxs-lookup"><span data-stu-id="e38d6-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="e38d6-109">**CalculationCanceled :** élevé lorsque l’utilisateur interrompt le calcul.</span><span class="sxs-lookup"><span data-stu-id="e38d6-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="e38d6-110">Le XLL arrête toutes les activités asynchrones.</span><span class="sxs-lookup"><span data-stu-id="e38d6-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="e38d6-111">Immédiatement après cet événement, **l’événement CalculationEnded** est lancé.</span><span class="sxs-lookup"><span data-stu-id="e38d6-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="e38d6-112">Pour gérer ces événements, le XLL utilise la fonction API C [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="e38d6-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e38d6-113">**CalculationEnded et** **CalculationCanceled** ne sont pas élevés lors du recalcul par programme.</span><span class="sxs-lookup"><span data-stu-id="e38d6-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

