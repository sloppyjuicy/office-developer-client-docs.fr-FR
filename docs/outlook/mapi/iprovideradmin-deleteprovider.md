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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: db09b44bd8eeeb3ab56513b1b9c2cab69f776002
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590084"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="fa143-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="fa143-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="fa143-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa143-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa143-105">Supprime un fournisseur de services à partir du service de message.</span><span class="sxs-lookup"><span data-stu-id="fa143-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="fa143-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa143-106">Parameters</span></span>

 <span data-ttu-id="fa143-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="fa143-107">_lpUID_</span></span>
  
> <span data-ttu-id="fa143-108">[entrée, sortie] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="fa143-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa143-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="fa143-109">Return value</span></span>

<span data-ttu-id="fa143-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa143-110">S_OK</span></span> 
  
> <span data-ttu-id="fa143-111">Le fournisseur a été supprimé du service de message.</span><span class="sxs-lookup"><span data-stu-id="fa143-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="fa143-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fa143-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fa143-113">Le **MAPIUID** désignés par le paramètre _lpUID_ n’a pas été reconnue.</span><span class="sxs-lookup"><span data-stu-id="fa143-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa143-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa143-114">Remarks</span></span>

<span data-ttu-id="fa143-115">La méthode **IProviderAdmin::DeleteProvider** supprime un fournisseur de services à partir du service de message.</span><span class="sxs-lookup"><span data-stu-id="fa143-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="fa143-116">**DeleteProvider** détermine le fournisseur de service à supprimer en faisant correspondre la structure **MAPIUID** désignée par _lpUID_ avec l’ensemble des identificateurs enregistré par les fournisseurs de service active.</span><span class="sxs-lookup"><span data-stu-id="fa143-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="fa143-117">La plupart des services de messagerie ne permettent pas de fournisseurs d’être supprimée alors que le profil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="fa143-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="fa143-118">Si le fournisseur à supprimer est en cours d’utilisation, **DeleteProvider** la marque pour suppression et non immédiatement et renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="fa143-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="fa143-119">Lorsque le fournisseur est n’est plus utilisé, il est supprimé.</span><span class="sxs-lookup"><span data-stu-id="fa143-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="fa143-120">**DeleteProvider** appelle la fonction de point d’entrée du message service avant que le fournisseur est supprimé à partir du service.</span><span class="sxs-lookup"><span data-stu-id="fa143-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="fa143-121">Le paramètre _ulContext_ est défini à MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="fa143-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="fa143-122">La fonction de point d’entrée de message service effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa143-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="fa143-123">Supprime le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="fa143-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="fa143-124">Supprime la section de profil du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="fa143-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="fa143-125">La fonction de point d’entrée de message service n’est pas encore appelée une fois que le fournisseur a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="fa143-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa143-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa143-126">See also</span></span>



[<span data-ttu-id="fa143-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fa143-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="fa143-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="fa143-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="fa143-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa143-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

