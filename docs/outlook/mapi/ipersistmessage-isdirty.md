---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407570"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="2610b-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="2610b-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="2610b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2610b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2610b-105">Recherche dans le formulaire les modifications apportées depuis le dernier sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2610b-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="2610b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2610b-106">Parameters</span></span>

<span data-ttu-id="2610b-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="2610b-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="2610b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2610b-108">Return value</span></span>

<span data-ttu-id="2610b-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="2610b-109">S_OK</span></span> 
  
> <span data-ttu-id="2610b-110">Le formulaire a des modifications qui ont été apportées depuis son dernier enregistré.</span><span class="sxs-lookup"><span data-stu-id="2610b-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="2610b-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2610b-111">S_FALSE</span></span> 
  
> <span data-ttu-id="2610b-112">Le formulaire ne comprend pas de modifications qui ont été apportées depuis son dernier enregistré.</span><span class="sxs-lookup"><span data-stu-id="2610b-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2610b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="2610b-113">Remarks</span></span>

<span data-ttu-id="2610b-114">Les visionneuses de formulaires appellent la méthode **IPersistMessage::IsDirty** pour déterminer si le message possède des données nonavées.</span><span class="sxs-lookup"><span data-stu-id="2610b-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2610b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2610b-115">See also</span></span>



[<span data-ttu-id="2610b-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2610b-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

