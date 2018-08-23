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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587844"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="d9fd4-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="d9fd4-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="d9fd4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9fd4-105">Établissement d’une banque de messages comme banque de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="d9fd4-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="d9fd4-106">Parameters</span></span>

 <span data-ttu-id="d9fd4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9fd4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d9fd4-108">[in] Masque de bits d’indicateurs qui contrôle le paramétrage de la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="d9fd4-109">Ces indicateurs sont mutuellement ; peut être défini qu’un seul des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="d9fd4-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="d9fd4-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d9fd4-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="d9fd4-111">Établit la banque de messages en tant que la valeur par défaut de la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="d9fd4-112">Met à jour la ligne de tableau d’état de la banque de messages en définissant l’indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9fd4-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="d9fd4-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="d9fd4-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="d9fd4-114">Définit la banque de messages comme le magasin à utiliser lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="d9fd4-115">Si la banque de messages n’est pas la banque par défaut, les clients doivent rendre la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="d9fd4-116">Met à jour la ligne de tableau d’état de la banque de messages en définissant l’indicateur STATUS_PRIMARY_STORE dans la colonne **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="d9fd4-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="d9fd4-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="d9fd4-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="d9fd4-118">Définit la banque de messages comme le magasin à utiliser lors de la connexion si la banque de messages principale n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="d9fd4-119">Si un client ne peut pas ouvrir la banque principale, il doit ouvrir le stockage secondaire et le définir en tant que la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="d9fd4-120">Met à jour la ligne de tableau d’état de la banque de messages en définissant l’indicateur STATUS_SECONDARY_STORE dans la colonne **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="d9fd4-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="d9fd4-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="d9fd4-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="d9fd4-122">Définit l’indicateur STATUS_SIMPLE_STORE dans **PR_RESOURCE_FLAGS** propriété du magasin message dans sa ligne de tableau d’état, ligne du tableau de magasin de message, dans le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="d9fd4-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="d9fd4-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="d9fd4-124">Définit l’indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la banque messages dans sa ligne tableau d’état et la ligne de tableau de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="d9fd4-125">Le profil n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="d9fd4-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9fd4-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="d9fd4-127">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d9fd4-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d9fd4-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9fd4-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="d9fd4-129">[in] Pointeur vers l’identificateur d’entrée de la banque de messages est destiné à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="d9fd4-130">Si un client passe _lpEntryID_NULL, aucune banque de messages n’est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9fd4-131">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d9fd4-131">Return value</span></span>

<span data-ttu-id="d9fd4-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9fd4-132">S_OK</span></span> 
  
> <span data-ttu-id="d9fd4-133">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9fd4-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9fd4-134">Remarks</span></span>

<span data-ttu-id="d9fd4-135">La méthode **IMAPISession::SetDefaultStore** établit une banque de messages comme une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9fd4-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="d9fd4-136">La banque de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="d9fd4-137">La banque de messages principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="d9fd4-138">Le magasin de message secondaire pour la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="d9fd4-139">Pour établir une banque de messages par défaut, la banque de messages doit avoir les indicateurs suivants définis dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) :</span><span class="sxs-lookup"><span data-stu-id="d9fd4-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="d9fd4-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="d9fd4-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="d9fd4-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="d9fd4-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="d9fd4-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="d9fd4-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d9fd4-143">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="d9fd4-143">Notes to callers</span></span>

<span data-ttu-id="d9fd4-144">Vous pouvez déterminer la banque de messages par défaut pour la session en récupérant la table d’état et en recherchant la valeur de l’indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="d9fd4-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="d9fd4-145">La ligne qui possède ce paramètre représente la banque de messages est désignée comme la valeur par défaut de la session.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="d9fd4-146">Lorsque la MAPI_DEFAULT_STORE ou l’indicateur MAPI_SIMPLE_STORE_PERMANENT est défini, MAPI met à jour le profil, table banque de messages et table d’état.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="d9fd4-147">Chaque fois qu’une modification est apportée à la valeur par défaut de banque de messages, les notifications suivantes sont générées :</span><span class="sxs-lookup"><span data-stu-id="d9fd4-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="d9fd4-148">Une notification d’événement **fnevTableModified** est émise pour chaque ligne concernée dans les deux le magasin et l’état de la table de messages.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="d9fd4-149">Une notification interne est émise au spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="d9fd4-150">Déjà en cours sont effectuées sans modification ; nouvelles opérations qui impliquent la banque de messages par défaut, telles que le téléchargement de message, sont traitées de la nouvelle banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9fd4-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d9fd4-151">MFCMAPI reference</span></span>

<span data-ttu-id="d9fd4-152">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9fd4-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d9fd4-153">**File**</span></span>|<span data-ttu-id="d9fd4-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d9fd4-154">**Function**</span></span>|<span data-ttu-id="d9fd4-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d9fd4-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9fd4-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d9fd4-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="d9fd4-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="d9fd4-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="d9fd4-158">MFCMAPI utilise la méthode **IMAPISession::SetDefaultStore** pour définir le magasin sélectionné en tant que la banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9fd4-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9fd4-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9fd4-159">See also</span></span>



[<span data-ttu-id="d9fd4-160">Propriété canonique PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="d9fd4-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="d9fd4-161">Propriété canonique PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="d9fd4-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="d9fd4-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9fd4-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="d9fd4-163">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9fd4-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="d9fd4-164">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d9fd4-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

