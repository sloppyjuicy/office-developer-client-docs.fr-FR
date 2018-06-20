---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783951"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="48189-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="48189-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="48189-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48189-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48189-105">Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité du principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="48189-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="48189-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48189-106">Parameters</span></span>

 <span data-ttu-id="48189-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="48189-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="48189-108">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="48189-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="48189-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="48189-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="48189-110">[out] Pointeur vers un pointeur vers l’identificateur d’entrée de l’objet qui fournit l’identité du principale.</span><span class="sxs-lookup"><span data-stu-id="48189-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48189-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="48189-111">Return value</span></span>

<span data-ttu-id="48189-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="48189-112">S_OK</span></span> 
  
> <span data-ttu-id="48189-113">L’identité du principale a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="48189-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="48189-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="48189-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="48189-115">L’appel a réussi, mais il n’existe aucune identité principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="48189-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="48189-116">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="48189-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="48189-117">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="48189-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="48189-118">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="48189-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48189-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="48189-119">Remarks</span></span>

<span data-ttu-id="48189-120">La méthode **IMAPISession::QueryIdentity** récupère l’identité du principale pour la session en cours et renvoie la valeur via le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="48189-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="48189-121">L’identité du principale est un objet, généralement un utilisateur de messagerie, qui représente l’utilisateur d’une session.</span><span class="sxs-lookup"><span data-stu-id="48189-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="48189-122">_lppEntryID_ renvoie l’identité du principale pour un objet [IMailUser](imailuserimapiprop.md) , qui est également stockée dans la propriété [PidTagEntryID](pidtagentryid-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="48189-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="48189-123">Vous pouvez utiliser la valeur renvoyée dans _lppEntryID_ pour ouvrir un objet **IMailUser** à l’aide de [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="48189-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="48189-124">Bien que plusieurs fournisseurs de services de plusieurs services de messagerie peuvent fournir l’identité du principale d’une session, MAPI désigne un fournisseur de service unique.</span><span class="sxs-lookup"><span data-stu-id="48189-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="48189-125">Le fournisseur de services qui fournit l’identité principale définit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="48189-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="48189-126">L’indicateur STATUS_PRIMARY_IDENTITY dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48189-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="48189-127">La propriété **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48189-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="48189-128">La propriété **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48189-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="48189-129">La propriété **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48189-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="48189-130">Si le fournisseur de services qui fournit l’identité du principale appartient à un service de message, les fournisseurs de services dans le service message également définir les propriétés PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="48189-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="48189-131">Ces propriétés sont publiées dans la table d’état de la session.</span><span class="sxs-lookup"><span data-stu-id="48189-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="48189-132">Si possible, **QueryIdentity** renvoie la valeur de la propriété **PR_IDENTITY_ENTRYID** à partir de la ligne d’état marquée avec STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="48189-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="48189-133">Si la propriété **PR_IDENTITY_ENTRYID** est manquante dans la ligne d’identité principale, **QueryIdentity** renvoie un identificateur d’entrée unique intégré avec d’autres informations de cette ligne.</span><span class="sxs-lookup"><span data-stu-id="48189-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="48189-134">Si l’indicateur STATUS_PRIMARY_IDENTITY est manquante à partir de toutes les colonnes dans la table d’état **PR_RESOURCE_FLAG** , **QueryIdentity** renvoie l’identificateur d’entrée première qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="48189-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="48189-135">Lorsqu’il n’existe aucun identificateur d’entrée appropriée à renvoyer, **QueryIdentity** réussit et l’avertissement MAPI_W_NO_SERVICE et pointe _lppEntryID_ vers un identificateur d’entrée codées en dur.</span><span class="sxs-lookup"><span data-stu-id="48189-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="48189-136">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="48189-136">Notes to callers</span></span>

<span data-ttu-id="48189-137">Vous pouvez appeler la méthode [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour assigner un service de message de la tâche de fournir l’identité principale de la session.</span><span class="sxs-lookup"><span data-stu-id="48189-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="48189-138">Une autre manière de récupérer l’identité principale est en recherchant la table d’état de la ligne avec les colonnes **PR_RESOURCE_FLAGS** définis sur STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="48189-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="48189-139">Pour plus d’informations sur cet autre façon de récupérer les informations d’identité, consultez la [Table d’état et les objets d’état](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="48189-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="48189-140">Lorsque vous avez terminé à l’aide de l’identificateur d’entrée pour l’identité du principale renvoyée par **QueryIdentity**, libérer la mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="48189-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="48189-141">Pour plus d’informations sur l’identité en général, voir [Identité principale MAPI](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="48189-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="48189-142">Pour plus d’informations sur la récupération d’identité de session MAPI, voir [récupération principal et le fournisseur d’identité](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="48189-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="48189-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="48189-143">MFCMAPI reference</span></span>

<span data-ttu-id="48189-144">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="48189-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="48189-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="48189-145">**File**</span></span>|<span data-ttu-id="48189-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="48189-146">**Function**</span></span>|<span data-ttu-id="48189-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="48189-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48189-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="48189-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="48189-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="48189-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="48189-150">MFCMAPI utilise la méthode **IMAPISession::QueryIdentity** pour ouvrir l’entrée du carnet d’adresses pour l’identité du principale de la session.</span><span class="sxs-lookup"><span data-stu-id="48189-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48189-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48189-151">See also</span></span>



[<span data-ttu-id="48189-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="48189-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="48189-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="48189-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="48189-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="48189-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="48189-155">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48189-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="48189-156">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="48189-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="48189-157">Identité principale MAPI</span><span class="sxs-lookup"><span data-stu-id="48189-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="48189-158">Extraction de principal et identité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="48189-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="48189-159">Utilisation de Macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="48189-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="48189-160">Table d’état et les objets d’état</span><span class="sxs-lookup"><span data-stu-id="48189-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

