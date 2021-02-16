---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426106"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="febcd-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="febcd-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="febcd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="febcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="febcd-105">Établit une magasin de messages comme magasin de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="febcd-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="febcd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="febcd-106">Parameters</span></span>

 <span data-ttu-id="febcd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="febcd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="febcd-108">[in] Masque de bits d’indicateurs qui contrôle le paramètre de la magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="febcd-109">Ces indicateurs s’excluent mutuellement ; Vous ne pouvez définir qu’un seul des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="febcd-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="febcd-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="febcd-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="febcd-111">Établit la magasin de messages comme la session par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="febcd-112">Met à jour la ligne de table d’état de la boutique de messages en STATUS_DEFAULT_STORE l’indicateur PR_RESOURCE_FLAGS **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="febcd-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="febcd-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="febcd-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="febcd-114">Établit la boutique de messages en tant que magasin à utiliser lors de l’ouverture de ouverture de ouverture de ligne.</span><span class="sxs-lookup"><span data-stu-id="febcd-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="febcd-115">Si la magasin de messages n’est pas la boutique par défaut, les clients doivent en faire la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="febcd-116">Met à jour la ligne de table d’état de la boutique de messages en STATUS_PRIMARY_STORE **l’indicateur** PR_RESOURCE_FLAGS colonne.</span><span class="sxs-lookup"><span data-stu-id="febcd-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="febcd-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="febcd-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="febcd-118">Établit la magasin de messages en tant que magasin à utiliser lors de l’ouverture de la boutique de messages si la boutique de messages principale n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="febcd-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="febcd-119">Si un client ne peut pas ouvrir le magasin principal, il doit ouvrir le magasin secondaire et le définir comme magasin par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="febcd-120">Met à jour la ligne de table d’état de la boutique de messages en STATUS_SECONDARY_STORE **l’indicateur** de PR_RESOURCE_FLAGS colonne.</span><span class="sxs-lookup"><span data-stu-id="febcd-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="febcd-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="febcd-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="febcd-122">Définit l’STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la boutique de messages dans sa ligne de table d’état, la ligne de table de la boutique de messages et dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="febcd-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="febcd-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="febcd-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="febcd-124">Définit l’STATUS_SIMPLE_STORE dans la propriété  PR_RESOURCE_FLAGS de la boutique de messages dans la ligne de table d’état et la ligne de table de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="febcd-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="febcd-125">Le profil n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="febcd-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="febcd-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="febcd-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="febcd-127">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="febcd-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="febcd-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="febcd-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="febcd-129">[in] Pointeur vers l’identificateur d’entrée de la magasin de messages prévu comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="febcd-130">Si un client transmet la valeur NULL dans  _lpEntryID,_ aucune magasine de messages n’est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="febcd-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="febcd-131">Return value</span></span>

<span data-ttu-id="febcd-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="febcd-132">S_OK</span></span> 
  
> <span data-ttu-id="febcd-133">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="febcd-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="febcd-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="febcd-134">Remarks</span></span>

<span data-ttu-id="febcd-135">La **méthode IMAPISession::SetDefaultStore** établit une magasin de messages comme l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="febcd-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="febcd-136">Magasin de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="febcd-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="febcd-137">Magasin de messages principal pour la session.</span><span class="sxs-lookup"><span data-stu-id="febcd-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="febcd-138">Magasin de messages secondaire pour la session.</span><span class="sxs-lookup"><span data-stu-id="febcd-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="febcd-139">Pour établir une magasin de messages comme magasin de messages par défaut, les indicateurs suivants doivent être définies dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) :</span><span class="sxs-lookup"><span data-stu-id="febcd-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="febcd-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="febcd-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="febcd-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="febcd-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="febcd-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="febcd-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="febcd-143">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="febcd-143">Notes to callers</span></span>

<span data-ttu-id="febcd-144">Vous pouvez déterminer la magasin de messages par défaut pour la session en récupérant la table d’état et en recherchant le paramètre de l’indicateur STATUS_DEFAULT_STORE dans la **colonne PR_RESOURCE_FLAGS.**</span><span class="sxs-lookup"><span data-stu-id="febcd-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="febcd-145">La ligne qui possède ce paramètre représente la magasin de messages désignée comme session par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="febcd-146">Lorsque l’MAPI_DEFAULT_STORE ou l’indicateur MAPI_SIMPLE_STORE_PERMANENT est définie, MAPI met à jour le profil, la table de la boutique de messages et la table d’état.</span><span class="sxs-lookup"><span data-stu-id="febcd-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="febcd-147">Chaque fois qu’une modification est apporté au paramètre par défaut de la boutique de messages, les notifications suivantes sont générées :</span><span class="sxs-lookup"><span data-stu-id="febcd-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="febcd-148">Une notification **d’événement fnevTableModified** est émise pour chaque ligne concernée dans la table d’état et la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="febcd-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="febcd-149">Une notification interne est émise aupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="febcd-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="febcd-150">Les opérations en cours sont terminées sans modification . les nouvelles opérations qui impliquent la magasin de messages par défaut, telles que le téléchargement des messages, sont traitées pour la nouvelle boutique par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="febcd-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="febcd-151">MFCMAPI reference</span></span>

<span data-ttu-id="febcd-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="febcd-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="febcd-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="febcd-153">**File**</span></span>|<span data-ttu-id="febcd-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="febcd-154">**Function**</span></span>|<span data-ttu-id="febcd-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="febcd-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="febcd-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="febcd-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="febcd-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="febcd-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="febcd-158">MFCMAPI utilise la méthode **IMAPISession::SetDefaultStore** pour définir le magasin sélectionné comme magasin par défaut.</span><span class="sxs-lookup"><span data-stu-id="febcd-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="febcd-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="febcd-159">See also</span></span>



[<span data-ttu-id="febcd-160">Propriété canonique PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="febcd-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="febcd-161">Propriété canonique PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="febcd-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="febcd-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="febcd-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="febcd-163">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="febcd-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="febcd-164">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="febcd-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

