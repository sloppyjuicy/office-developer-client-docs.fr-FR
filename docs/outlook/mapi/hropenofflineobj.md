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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347746"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="7c36a-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="7c36a-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="7c36a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c36a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c36a-105">Ouvre un objet hors connexion basé sur un profil donné.</span><span class="sxs-lookup"><span data-stu-id="7c36a-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7c36a-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7c36a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c36a-107">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="7c36a-107">Exported by:</span></span>  <br/> |<span data-ttu-id="7c36a-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="7c36a-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="7c36a-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7c36a-109">Called by:</span></span>  <br/> |<span data-ttu-id="7c36a-110">Client</span><span class="sxs-lookup"><span data-stu-id="7c36a-110">Client</span></span>  <br/> |
|<span data-ttu-id="7c36a-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7c36a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c36a-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="7c36a-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="7c36a-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c36a-113">Parameters</span></span>

 <span data-ttu-id="7c36a-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="7c36a-114">_ulReserved_</span></span>
  
> <span data-ttu-id="7c36a-115">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c36a-115">[in] This parameter is not used.</span></span> <span data-ttu-id="7c36a-116">Elle doit être 0.</span><span class="sxs-lookup"><span data-stu-id="7c36a-116">It must be 0.</span></span>
    
 <span data-ttu-id="7c36a-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="7c36a-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="7c36a-118">[in] Nom du profil pour l’objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7c36a-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="7c36a-119">Elle doit être exprimée en Unicode.</span><span class="sxs-lookup"><span data-stu-id="7c36a-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="7c36a-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="7c36a-120">_pGUID_</span></span>
  
> <span data-ttu-id="7c36a-121">[in] Pointeur vers un GUID qui peut être utilisé pour identifier de manière unique cet objet à partir d’autres objets hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7c36a-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="7c36a-122">Elle doit être **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="7c36a-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="7c36a-123">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="7c36a-123">_pReserved_</span></span>
  
> <span data-ttu-id="7c36a-124">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c36a-124">[in] This parameter is not used.</span></span> <span data-ttu-id="7c36a-125">Elle doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="7c36a-125">It must be **null**.</span></span>
    
 <span data-ttu-id="7c36a-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="7c36a-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="7c36a-127">[out] Pointeur vers l’objet hors connexion demandé.</span><span class="sxs-lookup"><span data-stu-id="7c36a-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="7c36a-128">L’appelant peut utiliser ce pointeur pour accéder à l’interface [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) pour rechercher les rappels pris en charge par cet objet et configurer des rappels pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7c36a-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7c36a-129">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7c36a-129">Return values</span></span>

<span data-ttu-id="7c36a-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c36a-130">S_OK</span></span> 
  
- <span data-ttu-id="7c36a-131">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="7c36a-131">The function call is successful.</span></span>
    
<span data-ttu-id="7c36a-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7c36a-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="7c36a-133">L’appel de fonction a échoué.</span><span class="sxs-lookup"><span data-stu-id="7c36a-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c36a-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c36a-134">Remarks</span></span>

<span data-ttu-id="7c36a-135">Il s’agit du premier appel qu’un client effectue lorsqu’il souhaite être averti des changements d’état de connexion pour un profil donné.</span><span class="sxs-lookup"><span data-stu-id="7c36a-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="7c36a-136">Lors de **l’appel de HrOpenOfflineObj,** le client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="7c36a-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="7c36a-137">Le client peut vérifier les types de rappels pris en charge par l’objet (à l’aide de [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), puis configurer les rappels pour celui-ci (à l’aide de [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="7c36a-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="7c36a-138">Lorsque vous [utilisez GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrOpenOfflineObj@20** comme nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="7c36a-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="7c36a-139">**HrOpenOfflineObj** fonctionne uniquement pour les clients qui sont des fournisseurs MAPI, des compl?ments COM et des extensions client Exchange en cours d’exécution dans le processus Outlook.</span><span class="sxs-lookup"><span data-stu-id="7c36a-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="7c36a-140">Dans le **cas contraire, HrOpenOfflineObj** renvoie **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="7c36a-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c36a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c36a-141">See also</span></span>



[<span data-ttu-id="7c36a-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c36a-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="7c36a-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="7c36a-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="7c36a-144">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="7c36a-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="7c36a-145">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7c36a-145">MAPI Constants</span></span>](mapi-constants.md)

