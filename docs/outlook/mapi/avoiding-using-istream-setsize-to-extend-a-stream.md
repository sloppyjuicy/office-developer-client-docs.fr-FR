---
title: Éviter d'utiliser IStreamSetSize pour étendre un flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331639"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="2cf71-103">Éviter d'utiliser IStream:: asSetS pour étendre un flux</span><span class="sxs-lookup"><span data-stu-id="2cf71-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="2cf71-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cf71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cf71-105">Lors de l'écriture dans des flux, il est parfois nécessaire de les agrandir car leur taille initiale n'est plus suffisante.</span><span class="sxs-lookup"><span data-stu-id="2cf71-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="2cf71-106">Utilisez la méthode OLE **IStream:: Write** pour effectuer cette opération au lieu de **IStream:: assets**.</span><span class="sxs-lookup"><span data-stu-id="2cf71-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="2cf71-107">**IStream:: Write** étend automatiquement le flux, en rendant \* \* IStream:: \* \* indésirable.</span><span class="sxs-lookup"><span data-stu-id="2cf71-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="2cf71-108">L'appel de **IStream:: Write** sans **IStream:: la méthode sets** peut prendre jusqu'à trois fois plus de temps que l'appel de la **méthode** avant l' **écriture**.</span><span class="sxs-lookup"><span data-stu-id="2cf71-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

