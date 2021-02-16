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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422102"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="6c734-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="6c734-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="6c734-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c734-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c734-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="6c734-105">Deprecated.</span></span> <span data-ttu-id="6c734-106">Attribue un nouveau nom à un service de message.</span><span class="sxs-lookup"><span data-stu-id="6c734-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="6c734-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c734-107">Parameters</span></span>

 <span data-ttu-id="6c734-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="6c734-108">_lpUID_</span></span>
  
> <span data-ttu-id="6c734-109">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à renommer.</span><span class="sxs-lookup"><span data-stu-id="6c734-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="6c734-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c734-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6c734-111">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="6c734-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6c734-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="6c734-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="6c734-113">[in] Pointeur vers le nouveau nom du service de message.</span><span class="sxs-lookup"><span data-stu-id="6c734-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c734-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6c734-114">Return value</span></span>

<span data-ttu-id="6c734-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6c734-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6c734-116">MAPI ne prend pas en charge le changement de nom de ce service de message.</span><span class="sxs-lookup"><span data-stu-id="6c734-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="6c734-117">**RenameMsgService** renvoie toujours cette valeur.</span><span class="sxs-lookup"><span data-stu-id="6c734-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6c734-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c734-118">Remarks</span></span>

<span data-ttu-id="6c734-119">Pour attribuer un nouveau nom à un service de message, les clients doivent utiliser la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) du service de message.</span><span class="sxs-lookup"><span data-stu-id="6c734-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="6c734-120">Les noms des fournisseurs de services dans un service de messagerie sont stockés dans leurs propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6c734-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c734-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c734-121">See also</span></span>



[<span data-ttu-id="6c734-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6c734-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6c734-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c734-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

