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
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576203"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="63b43-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="63b43-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="63b43-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63b43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63b43-105">Vérifie le formulaire pour que les modifications qui ont été apportées depuis le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="63b43-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="63b43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63b43-106">Parameters</span></span>

<span data-ttu-id="63b43-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="63b43-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="63b43-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63b43-108">Return value</span></span>

<span data-ttu-id="63b43-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="63b43-109">S_OK</span></span> 
  
> <span data-ttu-id="63b43-110">Le formulaire comporte des modifications qui ont été apportées depuis son dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="63b43-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="63b43-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="63b43-111">S_FALSE</span></span> 
  
> <span data-ttu-id="63b43-112">Le formulaire n’a pas de modifications qui ont été apportées depuis son dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="63b43-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63b43-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="63b43-113">Remarks</span></span>

<span data-ttu-id="63b43-114">Visionneuses de formulaire appeler la méthode **IPersistMessage::IsDirty** pour déterminer si le message comporte des données non enregistrées.</span><span class="sxs-lookup"><span data-stu-id="63b43-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63b43-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63b43-115">See also</span></span>



[<span data-ttu-id="63b43-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63b43-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

