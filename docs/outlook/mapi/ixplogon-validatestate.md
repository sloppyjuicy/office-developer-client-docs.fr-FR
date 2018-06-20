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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 165fe3a72060e88dc34d8153c13ae58bcbd9ae0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784529"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="356bb-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="356bb-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="356bb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="356bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="356bb-105">Vérifie l’état externe du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="356bb-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="356bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="356bb-106">Parameters</span></span>

 <span data-ttu-id="356bb-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="356bb-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="356bb-108">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="356bb-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="356bb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="356bb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="356bb-110">[in] Un masque de bits d’indicateurs qui contrôlent la façon dont le contrôle d’état est effectué et les résultats de la vérification du statut.</span><span class="sxs-lookup"><span data-stu-id="356bb-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="356bb-111">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="356bb-111">The following flags can be set:</span></span>
    
<span data-ttu-id="356bb-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="356bb-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="356bb-113">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="356bb-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="356bb-114">Le fournisseur de transport a la possibilité de continuer à travailler sur l’opération, ou elle peut annuler l’opération et retourner des MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="356bb-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="356bb-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="356bb-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="356bb-116">Valide l’état des fournisseurs de transport actuellement chargés en entraînant le spouleur MAPI appeler leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="356bb-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="356bb-117">Cet indicateur permet également le spouleur MAPI pour corriger les échecs de fournisseur de transport critique sans forcer les applications clientes et déconnectez-vous puis reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="356bb-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="356bb-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="356bb-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="356bb-119">L’utilisateur a sélectionné une opération de connexion.</span><span class="sxs-lookup"><span data-stu-id="356bb-119">The user selected a connect operation.</span></span> <span data-ttu-id="356bb-120">Lorsque cet indicateur est utilisé avec l’indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l’action de connexion se produit sans mise en cache.</span><span class="sxs-lookup"><span data-stu-id="356bb-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="356bb-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="356bb-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="356bb-122">L’utilisateur a sélectionné une opération de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="356bb-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="356bb-123">Lorsque cet indicateur est utilisé avec REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l’action de déconnexion se produit sans mise en cache.</span><span class="sxs-lookup"><span data-stu-id="356bb-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="356bb-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="356bb-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="356bb-125">Entrées de la table de cache d’en-tête doivent être traitées, tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="356bb-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="356bb-126">Messages MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE la valeur doivent être déplacés.</span><span class="sxs-lookup"><span data-stu-id="356bb-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="356bb-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="356bb-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="356bb-128">Une nouvelle liste d’en-têtes de message doit être téléchargée et statut du message tous les indicateurs de marquage doit être effacé.</span><span class="sxs-lookup"><span data-stu-id="356bb-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="356bb-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="356bb-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="356bb-130">Le fournisseur de transport empêche l’affichage d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="356bb-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="356bb-131">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="356bb-131">Return value</span></span>

<span data-ttu-id="356bb-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="356bb-132">S_OK</span></span> 
  
> <span data-ttu-id="356bb-133">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="356bb-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="356bb-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="356bb-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="356bb-135">Une autre opération est en cours ; Il doit être autorisé pour effectuer, ou il doit être arrêté avant cette opération est tentée.</span><span class="sxs-lookup"><span data-stu-id="356bb-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="356bb-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="356bb-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="356bb-137">Le fournisseur de transport à distance impliqué ne prend pas en charge une interface utilisateur et l’application cliente elle-même doit afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="356bb-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="356bb-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="356bb-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="356bb-139">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="356bb-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="356bb-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="356bb-140">Remarks</span></span>

<span data-ttu-id="356bb-141">Le spouleur MAPI appelle la méthode **IXPLogon::ValidateState** pour prendre en charge des appels à la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="356bb-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="356bb-142">Le fournisseur de transport doit répondre à l’appel **IXPLogon::ValidateState** exactement comme si le spouleur MAPI avait ouvert un objet d’état pour la session en cours et ensuite appelée **IMAPIStatus::ValidateState** sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="356bb-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="356bb-143">Pour prendre en charge son implémentation de **IMAPIStatus::ValidateState**, le spouleur MAPI appelle **IXPLogon::ValidateState** sur tous les objets d’ouverture de session pour tous les fournisseurs de transport actif qui sont en cours d’exécution dans une session de profil.</span><span class="sxs-lookup"><span data-stu-id="356bb-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="356bb-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="356bb-144">See also</span></span>



[<span data-ttu-id="356bb-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="356bb-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="356bb-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="356bb-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="356bb-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="356bb-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

