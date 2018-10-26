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
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586416"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="74b1b-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="74b1b-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="74b1b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74b1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74b1b-105">Enregistre le spouleur MAPI sur une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="74b1b-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="74b1b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74b1b-106">Parameters</span></span>

 <span data-ttu-id="74b1b-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="74b1b-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="74b1b-108">[in] Un pointeur vers l’interface MAPI prennent en charge l’objet de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="74b1b-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="74b1b-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="74b1b-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="74b1b-110">[in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="74b1b-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="74b1b-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="74b1b-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="74b1b-112">[in] Pointeur vers une chaîne qui contient le nom du profil utilisé pour l’ouverture de session MAPI spouleur.</span><span class="sxs-lookup"><span data-stu-id="74b1b-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="74b1b-113">Cette chaîne peut être affichée dans les boîtes de dialogue, écrite dans un fichier journal ou ignorée.</span><span class="sxs-lookup"><span data-stu-id="74b1b-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="74b1b-114">Si l’indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , elle doit être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="74b1b-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="74b1b-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="74b1b-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="74b1b-116">[in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="74b1b-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="74b1b-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="74b1b-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="74b1b-118">[in] Pointeur vers l’identificateur d’entrée de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="74b1b-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="74b1b-119">Passage de NULL dans le paramètre _lpEntryID_ indique qu’une banque de messages n’a pas encore été sélectionnée et que les boîtes de dialogue permettant à l’utilisateur de sélectionner une banque de messages peuvent être présentées.</span><span class="sxs-lookup"><span data-stu-id="74b1b-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="74b1b-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74b1b-120">_ulFlags_</span></span>
  
> <span data-ttu-id="74b1b-121">[in] Masque de bits d’indicateurs qui contrôle la façon dont les paramètres de connexion est effectuée.</span><span class="sxs-lookup"><span data-stu-id="74b1b-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="74b1b-122">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="74b1b-122">The following flags can be set:</span></span>
    
<span data-ttu-id="74b1b-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="74b1b-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="74b1b-124">L’appel est autorisé à fonctionne même si l’objet sous-jacent n’est pas disponible pour l’implémentation d’appel.</span><span class="sxs-lookup"><span data-stu-id="74b1b-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="74b1b-125">Si l’objet n’est pas disponible, un appel à l’objet suivant peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="74b1b-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="74b1b-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74b1b-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="74b1b-127">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="74b1b-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="74b1b-128">Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="74b1b-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="74b1b-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="74b1b-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="74b1b-130">Empêche l’affichage des boîtes de dialogue d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="74b1b-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="74b1b-131">Si cet indicateur est défini, la valeur d’erreur MAPI_E_LOGON_FAILED est renvoyée si l’ouverture de session échoue.</span><span class="sxs-lookup"><span data-stu-id="74b1b-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="74b1b-132">Si cet indicateur n’est pas défini, le fournisseur de banque de message peut inviter l’utilisateur à corriger un nom ou le mot de passe, à insérer un disque ou à effectuer d’autres actions nécessaires pour établir une connexion à la base.</span><span class="sxs-lookup"><span data-stu-id="74b1b-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="74b1b-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="74b1b-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="74b1b-134">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="74b1b-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="74b1b-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="74b1b-135">_lpInterface_</span></span>
  
> <span data-ttu-id="74b1b-136">[in] Pointeur vers l’identificateur d’interface (IID) pour la banque de messages pour vous connecter à.</span><span class="sxs-lookup"><span data-stu-id="74b1b-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="74b1b-137">Valeur null indique l’interface MAPI pour la banque de messages ([IMsgStore](imsgstoreimapiprop.md)) est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="74b1b-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="74b1b-138">Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour la banque de messages (par exemple IID_IUnknown ou IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="74b1b-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="74b1b-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="74b1b-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="74b1b-140">[in] Pointeur vers la taille, en octets, des données de validation dans le paramètre _lppbSpoolSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="74b1b-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="74b1b-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="74b1b-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="74b1b-142">[in] Pointeur vers un pointeur vers les données de validation.</span><span class="sxs-lookup"><span data-stu-id="74b1b-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="74b1b-143">La méthode **SpoolerLogon** utilise ces données pour ouvrir une session en tant que le fournisseur de banque de messages précédemment connecté à l’aide de la méthode [IMSProvider::Logon](imsprovider-logon.md) le spouleur MAPI sur le même magasin.</span><span class="sxs-lookup"><span data-stu-id="74b1b-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="74b1b-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="74b1b-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="74b1b-145">[out] Pointeur vers un pointeur vers la [MAPIERROR](mapierror.md) structure retournée, le cas échéant, qui contient des informations de version, composant et le contexte d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="74b1b-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="74b1b-146">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer.</span><span class="sxs-lookup"><span data-stu-id="74b1b-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="74b1b-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="74b1b-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="74b1b-148">[out] Un pointeur vers le pointeur vers le message stocker l’objet d’ouverture de session MAPI pour vous connecter à.</span><span class="sxs-lookup"><span data-stu-id="74b1b-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="74b1b-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="74b1b-149">_lppMDB_</span></span>
  
> <span data-ttu-id="74b1b-150">[out] Un pointeur vers le pointeur vers le message stocker d’objet pour les applications clientes pour vous connecter à spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="74b1b-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74b1b-151">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="74b1b-151">Return value</span></span>

<span data-ttu-id="74b1b-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="74b1b-152">S_OK</span></span> 
  
> <span data-ttu-id="74b1b-153">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="74b1b-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="74b1b-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="74b1b-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="74b1b-155">Le profil ne contient pas de suffisamment d’informations pour l’ouverture de session Terminer.</span><span class="sxs-lookup"><span data-stu-id="74b1b-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="74b1b-156">Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d’entrée du service de message du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="74b1b-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="74b1b-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="74b1b-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="74b1b-158">L’appel a réussi, mais le fournisseur de banque de messages a des informations d’erreur disponibles.</span><span class="sxs-lookup"><span data-stu-id="74b1b-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="74b1b-159">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="74b1b-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="74b1b-160">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="74b1b-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="74b1b-161">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="74b1b-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="74b1b-162">Pour obtenir les informations d’erreur à partir du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="74b1b-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="74b1b-163">Remarques</span><span class="sxs-lookup"><span data-stu-id="74b1b-163">Remarks</span></span>

<span data-ttu-id="74b1b-164">Le spouleur MAPI appelle la méthode **IMSProvider::SpoolerLogon** pour vous connecter à une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="74b1b-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="74b1b-165">Le spouleur MAPI doit utiliser l’objet de banque de messages renvoyé par le fournisseur de banque de messages dans le paramètre _lppMDB_ pendant et après l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="74b1b-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="74b1b-166">Pour des raisons de cohérence avec la méthode [IMSProvider::Logon](imsprovider-logon.md) , le fournisseur renvoie également un objet d’ouverture de session du magasin de message dans le paramètre _lppMSLogon_ .</span><span class="sxs-lookup"><span data-stu-id="74b1b-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="74b1b-167">L’utilisation de l’objet de magasin et l’objet d’ouverture de session sont identiques pour la banque habituelles d’ouverture de session ; une correspondance entre l’objet d’ouverture de session et l’objet de magasin doit être tels que les objets se comportent comme s’ils étaient un seul objet qui expose les deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="74b1b-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="74b1b-168">Les deux objets sont créés, ensemble et libérés ensemble.</span><span class="sxs-lookup"><span data-stu-id="74b1b-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="74b1b-169">Le fournisseur de banque doit marquer en interne de l’objet de banque de message renvoyé pour indiquer que le magasin est utilisé par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="74b1b-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="74b1b-170">Certaines des méthodes pour cet objet store se comportent différemment que pour le message magasin objet fourni aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="74b1b-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="74b1b-171">Cette marque interne est la méthode la plus courante de déclencher le comportement spécifique pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="74b1b-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74b1b-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74b1b-172">See also</span></span>



[<span data-ttu-id="74b1b-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="74b1b-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="74b1b-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="74b1b-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="74b1b-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74b1b-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

