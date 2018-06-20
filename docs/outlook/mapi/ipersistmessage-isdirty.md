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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784366"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="bd033-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="bd033-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="bd033-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd033-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd033-105">Vérifie le formulaire pour que les modifications qui ont été apportées depuis le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd033-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="bd033-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd033-106">Parameters</span></span>

<span data-ttu-id="bd033-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="bd033-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="bd033-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bd033-108">Return value</span></span>

<span data-ttu-id="bd033-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd033-109">S_OK</span></span> 
  
> <span data-ttu-id="bd033-110">Le formulaire comporte des modifications qui ont été apportées depuis son dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd033-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="bd033-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="bd033-111">S_FALSE</span></span> 
  
> <span data-ttu-id="bd033-112">Le formulaire n’a pas de modifications qui ont été apportées depuis son dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd033-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd033-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd033-113">Remarks</span></span>

<span data-ttu-id="bd033-114">Visionneuses de formulaire appeler la méthode **IPersistMessage::IsDirty** pour déterminer si le message comporte des données non enregistrées.</span><span class="sxs-lookup"><span data-stu-id="bd033-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd033-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd033-115">See also</span></span>



[<span data-ttu-id="bd033-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd033-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

