---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430573"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="5c638-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="5c638-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="5c638-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c638-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c638-105">Connecte lepooler MAPI à une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-105">Logs the MAPI spooler on to a message store.</span></span>
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a><span data-ttu-id="5c638-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c638-106">Parameters</span></span>

 <span data-ttu-id="5c638-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="5c638-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="5c638-108">[in] Pointeur vers l’objet de support MAPI pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="5c638-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5c638-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="5c638-110">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5c638-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="5c638-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="5c638-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="5c638-112">[in] Pointeur vers une chaîne qui contient le nom du profil utilisé pour la logo dupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c638-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="5c638-113">Cette chaîne peut être affichée dans des boîtes de dialogue, écrite dans un fichier journal ou simplement ignorée.</span><span class="sxs-lookup"><span data-stu-id="5c638-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="5c638-114">Elle doit être au format Unicode si l’MAPI_UNICODE est définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="5c638-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="5c638-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c638-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="5c638-116">[in] Taille, en octets, de l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="5c638-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5c638-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c638-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="5c638-118">[in] Pointeur vers l’identificateur d’entrée de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="5c638-119">La transmission de la valeur NULL dans le paramètre  _lpEntryID_ indique qu’une magasin de messages n’a pas encore été sélectionnée et que les boîtes de dialogue qui permettent à l’utilisateur de sélectionner une magasin de messages peuvent être présentées.</span><span class="sxs-lookup"><span data-stu-id="5c638-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="5c638-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c638-120">_ulFlags_</span></span>
  
> <span data-ttu-id="5c638-121">[in] Masque de bits d’indicateurs qui contrôle l’utilisation de l’logo.</span><span class="sxs-lookup"><span data-stu-id="5c638-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="5c638-122">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="5c638-122">The following flags can be set:</span></span>
    
<span data-ttu-id="5c638-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5c638-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5c638-124">L’appel est autorisé à réussir même si l’objet sous-jacent n’est pas disponible pour l’implémentation de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5c638-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="5c638-125">Si l’objet n’est pas disponible, un appel ultérieur à l’objet peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="5c638-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="5c638-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c638-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5c638-127">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c638-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5c638-128">Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="5c638-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="5c638-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5c638-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="5c638-130">Empêche l’affichage des boîtes de dialogue d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5c638-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="5c638-131">Si cet indicateur est définie, la valeur d’MAPI_E_LOGON_FAILED’erreur est renvoyée si l’échec de la logon.</span><span class="sxs-lookup"><span data-stu-id="5c638-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="5c638-132">Si cet indicateur n’est pas définie, le fournisseur de la boutique de messages peut inviter l’utilisateur à corriger un nom ou un mot de passe, à insérer un disque ou à effectuer d’autres actions nécessaires pour établir une connexion à la boutique.</span><span class="sxs-lookup"><span data-stu-id="5c638-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="5c638-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="5c638-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="5c638-134">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5c638-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="5c638-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5c638-135">_lpInterface_</span></span>
  
> <span data-ttu-id="5c638-136">[in] Pointeur vers l’identificateur d’interface (IID) de connexion à la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="5c638-137">La transmission de la valeur NULL indique que l’interface MAPI pour la magasin de messages ([IMsgStore](imsgstoreimapiprop.md)) est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="5c638-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="5c638-138">Le  _paramètre lpInterface_ peut également être définie sur un identificateur pour une interface appropriée pour la magasin de messages (par exemple, IID_IUnknown ou IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="5c638-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="5c638-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="5c638-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="5c638-140">[in] Pointeur vers la taille, en octets, des données de validation dans _le paramètre lppbSpoolSecurity._</span><span class="sxs-lookup"><span data-stu-id="5c638-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="5c638-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="5c638-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="5c638-142">[in] Pointeur vers un pointeur vers des données de validation.</span><span class="sxs-lookup"><span data-stu-id="5c638-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="5c638-143">La méthode **SpoolerLogon** utilise ces données pour connecter lepooler MAPI à la même boutique que le fournisseur de magasins de messages précédemment connecté à l’aide de la méthode [IMSProvider::Logon.](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="5c638-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="5c638-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="5c638-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="5c638-145">[out] Pointeur vers un pointeur vers la structure [MAPIERROR](mapierror.md) renvoyée, le caser, qui contient des informations de version, de composant et de contexte pour une erreur.</span><span class="sxs-lookup"><span data-stu-id="5c638-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="5c638-146">Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="5c638-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="5c638-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="5c638-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="5c638-148">[out] Pointeur vers le pointeur vers l’objet d’ouverture de session de la boutique de messages pour que MAPI se connecte.</span><span class="sxs-lookup"><span data-stu-id="5c638-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="5c638-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="5c638-149">_lppMDB_</span></span>
  
> <span data-ttu-id="5c638-150">[out] Pointeur vers le pointeur vers l’objet de magasin de messages pour lepooler MAPI et les applications clientes à connecter.</span><span class="sxs-lookup"><span data-stu-id="5c638-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c638-151">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5c638-151">Return value</span></span>

<span data-ttu-id="5c638-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c638-152">S_OK</span></span> 
  
> <span data-ttu-id="5c638-153">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="5c638-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5c638-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="5c638-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="5c638-155">Le profil ne contient pas suffisamment d’informations pour que la logon soit terminée.</span><span class="sxs-lookup"><span data-stu-id="5c638-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="5c638-156">Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d’entrée du service de messagerie du fournisseur de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="5c638-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="5c638-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="5c638-158">L’appel a réussi, mais des informations d’erreur sont disponibles pour le fournisseur de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="5c638-159">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="5c638-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5c638-160">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="5c638-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5c638-161">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="5c638-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="5c638-162">Pour obtenir les informations d’erreur du fournisseur, appelez la méthode [IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="5c638-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c638-163">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c638-163">Remarks</span></span>

<span data-ttu-id="5c638-164">Lepooler MAPI appelle la méthode **IMSProvider::SpoolerLogon** pour se connecter à une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="5c638-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="5c638-165">Lepooler MAPI doit utiliser l’objet de banque de messages renvoyé par le fournisseur de banque de messages dans le paramètre  _lppMDB_ pendant et après l’ouverture de connecté.</span><span class="sxs-lookup"><span data-stu-id="5c638-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="5c638-166">Pour des raisons de cohérence avec la méthode [IMSProvider::Logon,](imsprovider-logon.md) le fournisseur renvoie également un objet d’ouverture de messagerie dans le paramètre _lppMSLogon._</span><span class="sxs-lookup"><span data-stu-id="5c638-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="5c638-167">L’utilisation de l’objet store et de l’objet d’ouverture de ligne est identique pour l’ouverture de magasin habituelle . il doit y avoir une correspondance un-à-un entre l’objet d’ouverture de ligne et l’objet store afin que les objets agissent comme s’il s’agit d’un objet qui expose deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="5c638-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="5c638-168">Les deux objets sont créés ensemble et libérés ensemble.</span><span class="sxs-lookup"><span data-stu-id="5c638-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="5c638-169">Le fournisseur de magasin doit marquer en interne l’objet de magasin de messages renvoyé pour indiquer que la boutique est utilisée par lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c638-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="5c638-170">Certaines méthodes de cet objet store se comportent différemment de l’objet de magasin de messages fourni aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="5c638-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="5c638-171">Conserver cette marque interne est le moyen le plus courant de déclencher le comportement spécifique aupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c638-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c638-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c638-172">See also</span></span>



[<span data-ttu-id="5c638-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="5c638-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="5c638-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="5c638-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="5c638-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c638-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

