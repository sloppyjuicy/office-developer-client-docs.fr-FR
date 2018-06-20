---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f6461a1e47437c5d0c2c422d727e2b00819629b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783782"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="43d34-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="43d34-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="43d34-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43d34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43d34-105">Retourne un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.</span><span class="sxs-lookup"><span data-stu-id="43d34-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="43d34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43d34-106">Parameters</span></span>

 <span data-ttu-id="43d34-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="43d34-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="43d34-108">[out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="43d34-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43d34-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="43d34-109">Return value</span></span>

<span data-ttu-id="43d34-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="43d34-110">S_OK</span></span> 
  
> <span data-ttu-id="43d34-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="43d34-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43d34-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43d34-112">See also</span></span>



[<span data-ttu-id="43d34-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="43d34-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

