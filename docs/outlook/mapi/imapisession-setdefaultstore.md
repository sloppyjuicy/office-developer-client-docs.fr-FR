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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335804"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="10219-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="10219-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="10219-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10219-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10219-105">Établit une banque de messages comme banque de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="10219-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="10219-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10219-106">Parameters</span></span>

 <span data-ttu-id="10219-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10219-107">_ulFlags_</span></span>
  
> <span data-ttu-id="10219-108">dans Masque de réinitialisation des indicateurs qui contrôle le paramètre de la Banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="10219-109">Ces indicateurs s'excluent mutuellement; un seul des indicateurs suivants peut être défini:</span><span class="sxs-lookup"><span data-stu-id="10219-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="10219-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="10219-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="10219-111">Établit la Banque de messages comme valeur par défaut de la session.</span><span class="sxs-lookup"><span data-stu-id="10219-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="10219-112">Met à jour la ligne de table d'État du magasin de messages en définissant l'indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="10219-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="10219-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="10219-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="10219-114">Établit la Banque de messages comme banque à utiliser lors de l'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="10219-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="10219-115">S'il ne s'agit pas de la Banque de messages par défaut, les clients doivent le définir comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="10219-116">Met à jour la ligne de table d'État du magasin de messages en définissant l'indicateur STATUS_PRIMARY_STORE dans la colonne **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="10219-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="10219-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="10219-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="10219-118">Définit la Banque de messages comme banque à utiliser lors de l'ouverture de session si elle n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="10219-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="10219-119">Si un client ne peut pas ouvrir le magasin principal, il doit ouvrir le magasin secondaire et le définir par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="10219-120">Met à jour la ligne de table d'État du magasin de messages en définissant l'indicateur STATUS_SECONDARY_STORE dans la colonne **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="10219-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="10219-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="10219-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="10219-122">Définit l'indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la Banque de messages dans sa ligne de table d'État, sa ligne de table de magasin de messages et le profil de session.</span><span class="sxs-lookup"><span data-stu-id="10219-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="10219-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="10219-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="10219-124">Définit l'indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la Banque de messages dans sa ligne de table d'État et sa ligne de table de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="10219-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="10219-125">Le profil n'est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="10219-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="10219-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="10219-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="10219-127">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="10219-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="10219-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="10219-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="10219-129">dans Pointeur vers l'identificateur d'entrée de la Banque de messages qui est conçue comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="10219-130">Si un client transmet la valeur NULL dans _lpEntryID_, aucune banque de messages n'est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10219-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="10219-131">Return value</span></span>

<span data-ttu-id="10219-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="10219-132">S_OK</span></span> 
  
> <span data-ttu-id="10219-133">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="10219-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10219-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="10219-134">Remarks</span></span>

<span data-ttu-id="10219-135">La méthode **IMAPISession:: SetDefaultStore** établit une banque de messages de l'une des manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="10219-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="10219-136">Banque de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="10219-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="10219-137">Banque de messages principale de la session.</span><span class="sxs-lookup"><span data-stu-id="10219-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="10219-138">Banque de messages secondaire pour la session.</span><span class="sxs-lookup"><span data-stu-id="10219-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="10219-139">Pour établir une banque de messages par défaut, les indicateurs suivants doivent être définis dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la Banque de messages:</span><span class="sxs-lookup"><span data-stu-id="10219-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="10219-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="10219-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="10219-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="10219-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="10219-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="10219-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="10219-143">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="10219-143">Notes to callers</span></span>

<span data-ttu-id="10219-144">Vous pouvez déterminer la Banque de messages par défaut pour la session en récupérant la table d'État et en recherchant le paramètre de l'indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="10219-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="10219-145">La ligne qui contient ce paramètre représente la Banque de messages désignée comme session par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="10219-146">Lorsque l'indicateur MAPI_DEFAULT_STORE ou MAPI_SIMPLE_STORE_PERMANENT est défini, MAPI met à jour le profil, la table de banque de messages et la table d'État.</span><span class="sxs-lookup"><span data-stu-id="10219-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="10219-147">Chaque fois qu'une modification est apportée au paramètre par défaut de la Banque de messages, les notifications suivantes sont générées:</span><span class="sxs-lookup"><span data-stu-id="10219-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="10219-148">Une notification d'événement **fnevTableModified** est émise pour chaque ligne concernée dans la Banque de messages et le tableau d'État.</span><span class="sxs-lookup"><span data-stu-id="10219-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="10219-149">Une notification interne est émise pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="10219-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="10219-150">Les opérations déjà en cours sont effectuées sans modification; les nouvelles opérations qui impliquent la Banque de messages par défaut, telles que le téléchargement de messages, sont traitées pour le nouveau magasin par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="10219-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="10219-151">MFCMAPI reference</span></span>

<span data-ttu-id="10219-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="10219-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="10219-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="10219-153">**File**</span></span>|<span data-ttu-id="10219-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="10219-154">**Function**</span></span>|<span data-ttu-id="10219-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="10219-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10219-156">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="10219-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="10219-157">CMainDlg:: OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="10219-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="10219-158">MFCMAPI utilise la méthode **IMAPISession:: SetDefaultStore** pour définir la Banque sélectionnée comme banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="10219-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10219-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10219-159">See also</span></span>



[<span data-ttu-id="10219-160">Propriété canonique PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="10219-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="10219-161">Propriété canonique PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="10219-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="10219-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="10219-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="10219-163">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10219-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="10219-164">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="10219-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

