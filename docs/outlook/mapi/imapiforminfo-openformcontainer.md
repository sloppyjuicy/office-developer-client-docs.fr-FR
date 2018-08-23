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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 16e1d45806755bad8caff6847b0ecdea5b4ba78b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590420"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="90470-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="90470-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="90470-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90470-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90470-105">Retourne un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.</span><span class="sxs-lookup"><span data-stu-id="90470-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="90470-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90470-106">Parameters</span></span>

 <span data-ttu-id="90470-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="90470-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="90470-108">[out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="90470-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90470-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="90470-109">Return value</span></span>

<span data-ttu-id="90470-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="90470-110">S_OK</span></span> 
  
> <span data-ttu-id="90470-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="90470-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90470-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90470-112">See also</span></span>



[<span data-ttu-id="90470-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="90470-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

