---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784228"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="d9fdc-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="d9fdc-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="d9fdc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9fdc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9fdc-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-105">Deprecated.</span></span> <span data-ttu-id="d9fdc-106">Affecte un nouveau nom à un service de message.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="d9fdc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9fdc-107">Parameters</span></span>

 <span data-ttu-id="d9fdc-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d9fdc-108">_lpUID_</span></span>
  
> <span data-ttu-id="d9fdc-109">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message à renommer.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="d9fdc-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9fdc-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d9fdc-111">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d9fdc-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="d9fdc-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="d9fdc-113">[in] Pointeur vers le nouveau nom pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9fdc-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d9fdc-114">Return value</span></span>

<span data-ttu-id="d9fdc-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d9fdc-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d9fdc-116">MAPI ne gère pas la modification du nom de ce service de message.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="d9fdc-117">**RenameMsgService** renvoie toujours cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d9fdc-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9fdc-118">Remarks</span></span>

<span data-ttu-id="d9fdc-119">Pour attribuer un nouveau nom à un service de message, les clients doivent utiliser la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) du service de message.</span><span class="sxs-lookup"><span data-stu-id="d9fdc-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="d9fdc-120">Les noms des fournisseurs de services dans un service de message sont stockés dans leurs propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9fdc-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9fdc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9fdc-121">See also</span></span>



[<span data-ttu-id="d9fdc-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d9fdc-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d9fdc-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9fdc-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

