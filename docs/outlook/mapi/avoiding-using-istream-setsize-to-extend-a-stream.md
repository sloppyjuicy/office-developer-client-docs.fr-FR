---
title: Éviter d’utiliser IStreamSetSize pour étendre un flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428913"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="8afb9-103">Éviter d’utiliser IStream::SetSize pour étendre un flux</span><span class="sxs-lookup"><span data-stu-id="8afb9-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="8afb9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8afb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8afb9-105">Lors de l’écriture dans des flux, il est parfois nécessaire de les agrandir, car leur taille initiale n’est plus suffisante.</span><span class="sxs-lookup"><span data-stu-id="8afb9-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="8afb9-106">Utilisez la méthode OLE **IStream::Write** pour effectuer cette tâche plutôt que **IStream::SetSize**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="8afb9-107">**IStream::Write** étend automatiquement le flux, ce qui rend \*\* IStream::SetSize \*\* inutile.</span><span class="sxs-lookup"><span data-stu-id="8afb9-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="8afb9-108">Appeler **IStream::Write** sans **IStream::SetSize** peut être jusqu’à trois fois plus rapide que d’effectuer l’appel **SetSize** avant d’écrire. </span><span class="sxs-lookup"><span data-stu-id="8afb9-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

