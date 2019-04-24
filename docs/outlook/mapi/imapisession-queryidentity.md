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
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335692"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="b0895-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b0895-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="b0895-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0895-105">Renvoie l'identificateur d'entrée de l'objet qui fournit l'identité principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="b0895-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="b0895-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0895-106">Parameters</span></span>

 <span data-ttu-id="b0895-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b0895-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="b0895-108">remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b0895-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b0895-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="b0895-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="b0895-110">remarquer Pointeur vers un pointeur vers l'identificateur d'entrée de l'objet qui fournit l'identité principale.</span><span class="sxs-lookup"><span data-stu-id="b0895-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0895-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0895-111">Return value</span></span>

<span data-ttu-id="b0895-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0895-112">S_OK</span></span> 
  
> <span data-ttu-id="b0895-113">L'identité principale a été correctement renvoyée.</span><span class="sxs-lookup"><span data-stu-id="b0895-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="b0895-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b0895-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="b0895-115">L'appel a réussi, mais il n'existe pas d'identité principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="b0895-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="b0895-116">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="b0895-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b0895-117">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b0895-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b0895-118">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b0895-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0895-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0895-119">Remarks</span></span>

<span data-ttu-id="b0895-120">La méthode **IMAPISession:: QueryIdentity** extrait l'identité principale de la session en cours et renvoie la valeur via le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b0895-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="b0895-121">L'identité principale est un objet, généralement un utilisateur de messagerie, qui représente l'utilisateur d'une session.</span><span class="sxs-lookup"><span data-stu-id="b0895-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="b0895-122">_lppEntryID_ renvoie l'identité principale d'un objet [IMailUser](imailuserimapiprop.md) , qui est également stockée en tant que propriété [PidTagEntryID](pidtagentryid-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b0895-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="b0895-123">Vous pouvez utiliser la valeur renvoyée dans _lppEntryID_ pour ouvrir un objet **IMailUser** à l'aide de [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b0895-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="b0895-124">Bien que de nombreux fournisseurs de services dans plusieurs services de messagerie puissent fournir l'identité principale pour une session, MAPI désigne un seul fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b0895-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="b0895-125">Le fournisseur de services qui fournit l'identité principale définit les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b0895-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="b0895-126">L'indicateur STATUS_PRIMARY_IDENTITY dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0895-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b0895-127">Propriété **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0895-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b0895-128">Propriété **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0895-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b0895-129">Propriété **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0895-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="b0895-130">Si le fournisseur de services qui fournit l'identité principale appartient à un service de messagerie, les autres fournisseurs de services du service de messagerie définissent également les propriétés PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b0895-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="b0895-131">Ces propriétés sont publiées dans la table d'état de la session.</span><span class="sxs-lookup"><span data-stu-id="b0895-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="b0895-132">Dans la mesure du possible, **QueryIdentity** renvoie la valeur de la propriété **PR_IDENTITY_ENTRYID** à partir de la ligne d'État marquée avec STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b0895-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b0895-133">Si la propriété **PR_IDENTITY_ENTRYID** est absente de la ligne d'identité principale, **QueryIdentity** renvoie un identificateur d'entrée unique créé avec d'autres informations à partir de cette ligne.</span><span class="sxs-lookup"><span data-stu-id="b0895-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="b0895-134">Si l'indicateur STATUS_PRIMARY_IDENTITY est absent de toutes les colonnes **PR_RESOURCE_FLAG** de la table d'État, **QueryIdentity** renvoie le premier identificateur d'entrée qu'il trouve.</span><span class="sxs-lookup"><span data-stu-id="b0895-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="b0895-135">Lorsqu'il n'existe pas d'identificateur d'entrée approprié à renvoyer, **QueryIdentity** réussit avec l'avertissement MAPI_W_NO_SERVICE et pointe _lppEntryID_ vers un identificateur d'entrée codé en dur.</span><span class="sxs-lookup"><span data-stu-id="b0895-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0895-136">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="b0895-136">Notes to callers</span></span>

<span data-ttu-id="b0895-137">Vous pouvez appeler la méthode [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour affecter un service de message à la tâche de fourniture de l'identité principale de la session.</span><span class="sxs-lookup"><span data-stu-id="b0895-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="b0895-138">Pour récupérer l'identité principale, une autre méthode consiste à rechercher la ligne à l'aide des colonnes **PR_RESOURCE_FLAGS** définies sur STATUS_PRIMARY_IDENTITY dans la table d'État.</span><span class="sxs-lookup"><span data-stu-id="b0895-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b0895-139">Pour plus d'informations sur cette autre façon de récupérer des informations d'identité, voir [table d'État et objets d'État](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b0895-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="b0895-140">Lorsque vous avez terminé d'utiliser l'identificateur d'entrée pour l'identité principale renvoyée par **QueryIdentity**, libérez sa mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b0895-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b0895-141">Pour plus d'informations sur l'identité en général, consultez la rubrique [MAPI Primary Identity](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="b0895-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="b0895-142">Pour plus d'informations sur la récupération de l'identité de session MAPI, consultez la rubrique [extraction des identités principales et des fournisseurs](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="b0895-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b0895-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b0895-143">MFCMAPI reference</span></span>

<span data-ttu-id="b0895-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b0895-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b0895-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b0895-145">**File**</span></span>|<span data-ttu-id="b0895-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b0895-146">**Function**</span></span>|<span data-ttu-id="b0895-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b0895-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0895-148">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="b0895-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b0895-149">CMainDlg:: OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b0895-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="b0895-150">MFCMAPI utilise la méthode **IMAPISession:: QueryIdentity** pour ouvrir l'entrée de carnet d'adresses pour l'identité principale de la session.</span><span class="sxs-lookup"><span data-stu-id="b0895-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0895-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0895-151">See also</span></span>



[<span data-ttu-id="b0895-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b0895-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="b0895-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="b0895-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="b0895-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b0895-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b0895-155">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0895-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b0895-156">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b0895-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b0895-157">Identité principale MAPI</span><span class="sxs-lookup"><span data-stu-id="b0895-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="b0895-158">Récupération de l'identité principale et de l'identité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="b0895-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="b0895-159">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="b0895-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="b0895-160">Table d'État et objets d'État</span><span class="sxs-lookup"><span data-stu-id="b0895-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

