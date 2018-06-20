---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784388"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="833bc-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="833bc-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="833bc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="833bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="833bc-105">Supprime un fournisseur de services à partir du service de message.</span><span class="sxs-lookup"><span data-stu-id="833bc-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="833bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833bc-106">Parameters</span></span>

 <span data-ttu-id="833bc-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="833bc-107">_lpUID_</span></span>
  
> <span data-ttu-id="833bc-108">[entrée, sortie] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="833bc-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="833bc-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="833bc-109">Return value</span></span>

<span data-ttu-id="833bc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="833bc-110">S_OK</span></span> 
  
> <span data-ttu-id="833bc-111">Le fournisseur a été supprimé du service de message.</span><span class="sxs-lookup"><span data-stu-id="833bc-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="833bc-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="833bc-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="833bc-113">Le **MAPIUID** désignés par le paramètre _lpUID_ n’a pas été reconnue.</span><span class="sxs-lookup"><span data-stu-id="833bc-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="833bc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="833bc-114">Remarks</span></span>

<span data-ttu-id="833bc-115">La méthode **IProviderAdmin::DeleteProvider** supprime un fournisseur de services à partir du service de message.</span><span class="sxs-lookup"><span data-stu-id="833bc-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="833bc-116">**DeleteProvider** détermine le fournisseur de service à supprimer en faisant correspondre la structure **MAPIUID** désignée par _lpUID_ avec l’ensemble des identificateurs enregistré par les fournisseurs de service active.</span><span class="sxs-lookup"><span data-stu-id="833bc-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="833bc-117">La plupart des services de messagerie ne permettent pas de fournisseurs d’être supprimée alors que le profil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="833bc-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="833bc-118">Si le fournisseur à supprimer est en cours d’utilisation, **DeleteProvider** la marque pour suppression et non immédiatement et renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="833bc-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="833bc-119">Lorsque le fournisseur est n’est plus utilisé, il est supprimé.</span><span class="sxs-lookup"><span data-stu-id="833bc-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="833bc-120">**DeleteProvider** appelle la fonction de point d’entrée du message service avant que le fournisseur est supprimé à partir du service.</span><span class="sxs-lookup"><span data-stu-id="833bc-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="833bc-121">Le paramètre _ulContext_ est défini à MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="833bc-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="833bc-122">La fonction de point d’entrée de message service effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="833bc-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="833bc-123">Supprime le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="833bc-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="833bc-124">Supprime la section de profil du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="833bc-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="833bc-125">La fonction de point d’entrée de message service n’est pas encore appelée une fois que le fournisseur a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="833bc-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="833bc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="833bc-126">See also</span></span>



[<span data-ttu-id="833bc-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="833bc-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="833bc-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="833bc-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="833bc-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="833bc-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

