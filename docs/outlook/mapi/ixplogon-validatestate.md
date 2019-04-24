---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351568"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="f3351-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f3351-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="f3351-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3351-105">Vérifie l'état externe du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="f3351-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f3351-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3351-106">Parameters</span></span>

 <span data-ttu-id="f3351-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f3351-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f3351-108">dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="f3351-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="f3351-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3351-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f3351-110">dans Masque de des indicateurs qui contrôle le mode d'exécution du contrôle d'État et les résultats de la vérification de l'État.</span><span class="sxs-lookup"><span data-stu-id="f3351-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="f3351-111">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="f3351-111">The following flags can be set:</span></span>
    
<span data-ttu-id="f3351-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="f3351-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="f3351-113">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f3351-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="f3351-114">Le fournisseur de transport a la possibilité de continuer à travailler sur l'opération, ou il peut abandonner l'opération et renvoyer MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="f3351-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="f3351-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="f3351-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="f3351-116">Valide l'état des fournisseurs de transport actuellement chargés en provoquant l'appel de la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3351-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="f3351-117">Cet indicateur permet également au spouleur MAPI de corriger les échecs de fournisseur de transport critiques sans forcer les applications clientes à se déconnecter, puis à se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="f3351-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="f3351-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="f3351-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="f3351-119">L'utilisateur a sélectionné une opération de connexion.</span><span class="sxs-lookup"><span data-stu-id="f3351-119">The user selected a connect operation.</span></span> <span data-ttu-id="f3351-120">Lorsque cet indicateur est utilisé avec l'indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l'action de connexion se produit sans mise en cache.</span><span class="sxs-lookup"><span data-stu-id="f3351-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="f3351-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="f3351-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="f3351-122">L'utilisateur a sélectionné une opération de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="f3351-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="f3351-123">Lorsque cet indicateur est utilisé avec REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l'action de déconnexion se produit sans mise en cache.</span><span class="sxs-lookup"><span data-stu-id="f3351-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="f3351-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f3351-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f3351-125">Les entrées de la table de cache d'en-tête doivent être traitées, tous les messages marqués avec l'indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l'indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="f3351-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="f3351-126">Les messages qui ont à la fois MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE doivent être déplacés.</span><span class="sxs-lookup"><span data-stu-id="f3351-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="f3351-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f3351-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f3351-128">Une nouvelle liste d'en-têtes de message doit être téléchargée et tous les indicateurs de marquage d'état de message doivent être effacés.</span><span class="sxs-lookup"><span data-stu-id="f3351-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="f3351-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="f3351-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="f3351-130">Empêche le fournisseur de transport d'afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3351-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3351-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3351-131">Return value</span></span>

<span data-ttu-id="f3351-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3351-132">S_OK</span></span> 
  
> <span data-ttu-id="f3351-133">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="f3351-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="f3351-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f3351-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f3351-135">Une autre opération est en cours; il doit être autorisé à se terminer ou doit être arrêté avant la tentative de cette opération.</span><span class="sxs-lookup"><span data-stu-id="f3351-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="f3351-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f3351-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f3351-137">Le fournisseur de transport distant impliqué ne prend pas en charge une interface utilisateur et l'application cliente elle-même doit afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f3351-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="f3351-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f3351-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f3351-139">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f3351-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f3351-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3351-140">Remarks</span></span>

<span data-ttu-id="f3351-141">Le spouleur MAPI appelle la méthode **IXPLogon:: ValidateState** pour prendre en charge les appels à la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) pour l'objet Status.</span><span class="sxs-lookup"><span data-stu-id="f3351-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="f3351-142">Le fournisseur de transport doit répondre à l'appel **IXPLogon:: ValidateState** exactement comme si le spouleur MAPI avait ouvert un objet d'État pour la session en cours, puis il a appelé **IMAPIStatus:: ValidateState** sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="f3351-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="f3351-143">Pour prendre en charge son implémentation de **IMAPIStatus:: ValidateState**, le spouleur MAPI appelle **IXPLogon:: ValidateState** sur tous les objets d'ouverture de session pour tous les fournisseurs de transport actifs qui s'exécutent dans une session de profil.</span><span class="sxs-lookup"><span data-stu-id="f3351-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3351-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3351-144">See also</span></span>



[<span data-ttu-id="f3351-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f3351-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="f3351-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="f3351-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="f3351-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3351-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

