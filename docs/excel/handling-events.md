---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782123"
---
# <a name="handling-events"></a><span data-ttu-id="1ba3c-103">Gestion d'événements</span><span class="sxs-lookup"><span data-stu-id="1ba3c-103">Handling Events</span></span>

 <span data-ttu-id="1ba3c-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1ba3c-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1ba3c-105">À compter d’Excel 2010, XLL peuvent recevoir des événements conçus pour gérer le cycle de vie de fonction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="1ba3c-106">Les événements sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="1ba3c-106">The events are as follows:</span></span>
  
- <span data-ttu-id="1ba3c-107">**CalculationEnded**: déclenché lors de la fin du calcul.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="1ba3c-108">Après cet événement, vous pouvez libérer les ressources allouées au cours du calcul.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="1ba3c-109">**CalculationCanceled**: déclenché lorsque l’utilisateur interrompt le calcul.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="1ba3c-110">La ressource XLL arrête toutes les activités asynchrones.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="1ba3c-111">Immédiatement après cet événement, l’événement **CalculationEnded** est déclenché.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="1ba3c-112">Pour gérer ces événements, le XLL utilise la fonction de API C [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="1ba3c-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1ba3c-113">**CalculationEnded** et **CalculationCanceled** ne sont pas déclenchés lors d’un recalcul par programme.</span><span class="sxs-lookup"><span data-stu-id="1ba3c-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

