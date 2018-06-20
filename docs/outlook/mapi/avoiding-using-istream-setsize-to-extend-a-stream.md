---
title: Éviter d’étendre un flux de données à l’aide de IStreamSetSize
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782995"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="a9143-103">Éviter d’étendre un flux de données à l’aide de IStream::SetSize</span><span class="sxs-lookup"><span data-stu-id="a9143-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="a9143-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9143-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9143-105">Lors de l’écriture dans les flux, il est parfois nécessaire de les agrandir, car leur taille initiale n’est plus suffisante.</span><span class="sxs-lookup"><span data-stu-id="a9143-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="a9143-106">Pour cela, utiliser la méthode OLE **IStream::Write** plutôt que **IStream::SetSize**.</span><span class="sxs-lookup"><span data-stu-id="a9143-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="a9143-107">**IStream::Write** étend automatiquement le flux, rendant ** IStream::SetSize ** inutiles.</span><span class="sxs-lookup"><span data-stu-id="a9143-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="a9143-108">Appel **IStream::Write** sans **IStream::SetSize** la peut être plus rapide que la **SetSize** avant **d’écrire**des appels jusqu'à trois fois.</span><span class="sxs-lookup"><span data-stu-id="a9143-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

