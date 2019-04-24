---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347746"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="01d95-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="01d95-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="01d95-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01d95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01d95-105">Ouvre un objet hors connexion basé sur un profil donné.</span><span class="sxs-lookup"><span data-stu-id="01d95-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="01d95-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="01d95-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01d95-107">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="01d95-107">Exported by:</span></span>  <br/> |<span data-ttu-id="01d95-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="01d95-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="01d95-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="01d95-109">Called by:</span></span>  <br/> |<span data-ttu-id="01d95-110">Client</span><span class="sxs-lookup"><span data-stu-id="01d95-110">Client</span></span>  <br/> |
|<span data-ttu-id="01d95-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="01d95-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="01d95-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="01d95-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="01d95-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01d95-113">Parameters</span></span>

 <span data-ttu-id="01d95-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="01d95-114">_ulReserved_</span></span>
  
> <span data-ttu-id="01d95-115">dans Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="01d95-115">[in] This parameter is not used.</span></span> <span data-ttu-id="01d95-116">Il doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="01d95-116">It must be 0.</span></span>
    
 <span data-ttu-id="01d95-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="01d95-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="01d95-118">dans Nom du profil pour lequel l'objet hors connexion est destiné.</span><span class="sxs-lookup"><span data-stu-id="01d95-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="01d95-119">Il doit être exprimé en Unicode.</span><span class="sxs-lookup"><span data-stu-id="01d95-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="01d95-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="01d95-120">_pGUID_</span></span>
  
> <span data-ttu-id="01d95-121">dans Pointeur vers un GUID qui peut être utilisé pour identifier cet objet de manière unique à partir d'autres objets hors connexion.</span><span class="sxs-lookup"><span data-stu-id="01d95-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="01d95-122">Il doit être **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="01d95-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="01d95-123">_Disparition_</span><span class="sxs-lookup"><span data-stu-id="01d95-123">_pReserved_</span></span>
  
> <span data-ttu-id="01d95-124">dans Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="01d95-124">[in] This parameter is not used.</span></span> <span data-ttu-id="01d95-125">Elle doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="01d95-125">It must be **null**.</span></span>
    
 <span data-ttu-id="01d95-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="01d95-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="01d95-127">remarquer Pointeur vers l'objet hors connexion demandé.</span><span class="sxs-lookup"><span data-stu-id="01d95-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="01d95-128">L'appelant peut utiliser ce pointeur pour accéder à l'interface [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) pour rechercher les rappels pris en charge par cet objet et pour configurer des rappels pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="01d95-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="01d95-129">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="01d95-129">Return values</span></span>

<span data-ttu-id="01d95-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="01d95-130">S_OK</span></span> 
  
- <span data-ttu-id="01d95-131">L'appel de fonction est réussi.</span><span class="sxs-lookup"><span data-stu-id="01d95-131">The function call is successful.</span></span>
    
<span data-ttu-id="01d95-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="01d95-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="01d95-133">Échec de l'appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="01d95-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01d95-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="01d95-134">Remarks</span></span>

<span data-ttu-id="01d95-135">Il s'agit du premier appel qu'un client effectue lorsque le client souhaite être informé des modifications d'état de connexion pour un profil donné.</span><span class="sxs-lookup"><span data-stu-id="01d95-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="01d95-136">Lors de l'appel de **HrOpenOfflineObj**, le client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="01d95-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="01d95-137">Le client peut vérifier les genres de rappels pris en charge par l'objet (à l'aide de [IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)), puis configurer des rappels pour lui (à l'aide de [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="01d95-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="01d95-138">Lors de l'utilisation de [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) pour Rechercher l'adresse de cette fonction dans msmapi32. dll, spécifiez **HrOpenOfflineObj @ 20** comme nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="01d95-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="01d95-139">**HrOpenOfflineObj** fonctionne uniquement pour les clients qui sont des fournisseurs MAPI, des compléments COM et des extensions client Exchange en cours d'exécution dans le processus Outlook.</span><span class="sxs-lookup"><span data-stu-id="01d95-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="01d95-140">Sinon, **HrOpenOfflineObj** renvoie **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="01d95-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01d95-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d95-141">See also</span></span>



[<span data-ttu-id="01d95-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01d95-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="01d95-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="01d95-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="01d95-144">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="01d95-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="01d95-145">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="01d95-145">MAPI Constants</span></span>](mapi-constants.md)

