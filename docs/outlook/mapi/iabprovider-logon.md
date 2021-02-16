---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348782"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="822bd-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="822bd-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="822bd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="822bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="822bd-105">Établit une connexion à une session active.</span><span class="sxs-lookup"><span data-stu-id="822bd-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="822bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="822bd-106">Parameters</span></span>

 <span data-ttu-id="822bd-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="822bd-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="822bd-108">[in] Pointeur vers l’objet de support du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="822bd-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="822bd-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="822bd-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="822bd-110">[in] Poignée vers la fenêtre parente de la boîte de dialogue d’ouverture de conversation que la méthode **Logon** affiche, si elle est autorisée.</span><span class="sxs-lookup"><span data-stu-id="822bd-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="822bd-111">Le _paramètre ulUIParam_ contient la valeur du paramètre du même nom transmis à MAPI dans l’appel précédent à la [fonction MAPILogonEx.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="822bd-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="822bd-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="822bd-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="822bd-113">[in] Pointeur vers le nom du profil de session.</span><span class="sxs-lookup"><span data-stu-id="822bd-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="822bd-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="822bd-114">_ulFlags_</span></span>
  
> <span data-ttu-id="822bd-115">[in] Masque de bits d’indicateurs qui contrôle l’utilisation de l’logo.</span><span class="sxs-lookup"><span data-stu-id="822bd-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="822bd-116">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="822bd-116">The following flags can be set:</span></span>
    
<span data-ttu-id="822bd-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="822bd-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="822bd-118">Le fournisseur ne doit pas afficher de boîte de dialogue pendant l’accès.</span><span class="sxs-lookup"><span data-stu-id="822bd-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="822bd-119">Si cet indicateur n’est pas définie, le fournisseur peut afficher une boîte de dialogue pour informer l’utilisateur de l’absence d’informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="822bd-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="822bd-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="822bd-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="822bd-121">Permet à **l’utilisateur de** renvoyer correctement l’opération, éventuellement avant la fin du processus d’logonisation.</span><span class="sxs-lookup"><span data-stu-id="822bd-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="822bd-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="822bd-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="822bd-123">Toutes les chaînes doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="822bd-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="822bd-124">Si l’MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="822bd-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="822bd-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="822bd-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="822bd-126">[in, out] Pointeur vers la taille, en octets, de la structure des informations d’identification de sécurité pointée par _le paramètre lppbSecurity._</span><span class="sxs-lookup"><span data-stu-id="822bd-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="822bd-127">Lors de l’entrée, la valeur doit être non zéro ; lors de la sortie, la valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="822bd-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="822bd-128">Dans les deux cas, les pointeurs doivent être valides.</span><span class="sxs-lookup"><span data-stu-id="822bd-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="822bd-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="822bd-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="822bd-130">[in, out] Pointeur vers un pointeur vers les informations d’identification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="822bd-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="822bd-131">Lors de l’entrée, la valeur doit être non zéro ; lors de la sortie, la valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="822bd-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="822bd-132">Dans les deux cas, le pointeur doit être valide.</span><span class="sxs-lookup"><span data-stu-id="822bd-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="822bd-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="822bd-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="822bd-134">[out] Pointeur vers un pointeur vers une structure [MAPIERROR.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="822bd-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="822bd-135">Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="822bd-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="822bd-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="822bd-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="822bd-137">[out] Pointeur vers un pointeur vers l’objet d’logo du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="822bd-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="822bd-138">Return value</span></span>

<span data-ttu-id="822bd-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="822bd-139">S_OK</span></span> 
  
> <span data-ttu-id="822bd-140">Une connexion à une session active a été établie avec succès.</span><span class="sxs-lookup"><span data-stu-id="822bd-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="822bd-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="822bd-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="822bd-142">Le fournisseur ne peut pas se connecter, mais MAPI peut continuer à se connecter aux autres fournisseurs dans le service de messagerie auquel il appartient.</span><span class="sxs-lookup"><span data-stu-id="822bd-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="822bd-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="822bd-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="822bd-144">Le fournisseur ne dispose pas d’informations suffisantes pour terminer l’accès.</span><span class="sxs-lookup"><span data-stu-id="822bd-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="822bd-145">MAPI appelle la fonction d’entrée de service de messagerie du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="822bd-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="822bd-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="822bd-147">Le serveur n’est pas configuré pour prendre en charge la page de code du client.</span><span class="sxs-lookup"><span data-stu-id="822bd-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="822bd-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="822bd-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="822bd-149">Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.</span><span class="sxs-lookup"><span data-stu-id="822bd-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="822bd-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="822bd-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="822bd-151">L’utilisateur a annulé l’opération,  généralement en cliquant sur le bouton Annuler dans la boîte de dialogue d’ouverture de conversation.</span><span class="sxs-lookup"><span data-stu-id="822bd-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="822bd-152">Remarques</span><span class="sxs-lookup"><span data-stu-id="822bd-152">Remarks</span></span>

<span data-ttu-id="822bd-153">Les connexions sont établies avec chaque fournisseur de carnet d’adresses dans le profil de session lorsqu’un client appelle la méthode [IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md)</span><span class="sxs-lookup"><span data-stu-id="822bd-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="822bd-154">**OpenAddressBook** appelle ensuite la méthode **Logon** de chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="822bd-155">Le nom de profil pointé par le paramètre _lpszProfileName_ s’affiche dans le jeu de caractères du client de l’utilisateur, comme indiqué par la présence ou l’absence de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="822bd-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="822bd-156">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="822bd-156">Notes to implementers</span></span>

<span data-ttu-id="822bd-157">Dans votre implémentation de la méthode **Logon,** appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire un identificateur unique ou une structure [MAPIUID.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="822bd-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="822bd-158">Chacun de vos objets aura un identificateur d’entrée qui inclut ce **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="822bd-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="822bd-159">MAPI utilise **MAPIUID** pour faire correspondre un objet à son fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="822bd-160">Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un utilisateur de messagerie, **OpenEntry** examine la partie **MAPIUID** de l’identificateur d’entrée qui a été passé et la correspond à un **MAPIUID** enregistré par un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="822bd-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="822bd-161">Si un client se connecte à votre fournisseur plusieurs fois, vous pouvez inscrire un **MAPIUID** différent pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="822bd-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="822bd-162">L’inscription de structures **MAPIUID** uniques permet à MAPI d’router correctement les demandes vers l’instance de fournisseur appropriée.</span><span class="sxs-lookup"><span data-stu-id="822bd-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="822bd-163">Toutefois, vous souhaitez peut-être que chaque objet d' logon partage un **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="822bd-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="822bd-164">Dans ce cas, vous devez être en mesure de gérer le routage vous-même au lieu de vous appuyer sur MAPI.</span><span class="sxs-lookup"><span data-stu-id="822bd-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="822bd-165">Pour plus d’informations sur la création **d’un MAPIUID,** voir [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="822bd-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="822bd-166">L’objet de prise en charge que MAPI transmet à votre méthode **Logon** dans le paramètre _lpMAPISup_ permet d’accéder à de nombreuses méthodes incluses dans l’interface [IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="822bd-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="822bd-167">MAPI crée un objet de support personnalisé pour votre type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="822bd-168">Par exemple, si vous devez vous connecter à un système de messagerie ou à un service d’annuaire sous-jacent lorsque vous établissez votre connexion, vous pouvez appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour récupérer les informations d’identification de sécurité pour cette session d’ouverture de session particulière.</span><span class="sxs-lookup"><span data-stu-id="822bd-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="822bd-169">Si **l’logon** est réussi, assurez-vous d’appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l’objet de support pour incrémenter son nombre de références.</span><span class="sxs-lookup"><span data-stu-id="822bd-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="822bd-170">Cela permet à votre fournisseur de conserver le pointeur d’objet de prise en charge pour le reste de la session.</span><span class="sxs-lookup"><span data-stu-id="822bd-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="822bd-171">Si vous n’appelez pas cette **méthode AddRef,** MAPI déchargera votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="822bd-172">Vous pouvez inclure le nom de profil transmis dans le paramètre  _lpszProfileName_ dans les boîtes de dialogue d’erreur, les écrans d’accès ou d’autres interfaces utilisateur.</span><span class="sxs-lookup"><span data-stu-id="822bd-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="822bd-173">Pour utiliser le nom de profil, copiez-le dans le stockage que vous avez alloué.</span><span class="sxs-lookup"><span data-stu-id="822bd-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="822bd-174">Créez un objet de logo et renvoyez un pointeur vers celui-ci dans le _paramètre lppABLogon._</span><span class="sxs-lookup"><span data-stu-id="822bd-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="822bd-175">MAPI utilise cet objet de logon pour appeler les méthodes dans votre [implémentation IABLogon.](iablogoniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="822bd-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="822bd-176">Si vous avez besoin d’un mot de passe lors de l’affichage, affichez une boîte de dialogue d’AB_NO_DIALOG si l’indicateur de AB_NO_DIALOG n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="822bd-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="822bd-177">Si l’utilisateur annule le processus d’MAPI_E_USER_CANCEL, en cliquant généralement sur le bouton Annuler dans la boîte de dialogue. </span><span class="sxs-lookup"><span data-stu-id="822bd-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="822bd-178">En règle générale, lorsqu’un fournisseur de carnet d’adresses ne peut pas se connecter, MAPI désactive le service de messagerie auquel appartient le fournisseur défaillant, autrement dit, MAPI ne tente pas d’établir de connexions pour les autres fournisseurs qui appartiennent au service pendant le reste de la durée de vie de la session.</span><span class="sxs-lookup"><span data-stu-id="822bd-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="822bd-179">Toutefois, si votre fournisseur ne peut pas établir de connexion et que vous ne souhaitez pas désactiver l’intégralité du service, renvoyez MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="822bd-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="822bd-180">MAPI ne désactive pas le service de messagerie auquel appartient le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="822bd-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="822bd-181">Renvoyer MAPI_E_FAILONEPROVIDER si une erreur se produit et n’est pas suffisamment grave pour empêcher les autres fournisseurs du service de messagerie d’établir des connexions.</span><span class="sxs-lookup"><span data-stu-id="822bd-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="822bd-182">Renvoyer MAPI_E_UNCONFIGURED si les informations de configuration nécessaires sont manquantes dans le profil et que vous ne pouvez pas afficher de boîte de dialogue pour inviter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="822bd-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="822bd-183">MAPI répond en appelant la fonction de point d’entrée du service de messagerie de votre fournisseur avec MSG_SERVICE_CONFIGURE définie en tant que paramètre  _ulContext_ pour donner au service la possibilité de se configurer lui-même, par programme ou à l’aide d’une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="822bd-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="822bd-184">Lorsque la fonction de point d’entrée du service de message est terminée, MAPI esse la nouvelle fois.</span><span class="sxs-lookup"><span data-stu-id="822bd-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="822bd-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="822bd-185">See also</span></span>



[<span data-ttu-id="822bd-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="822bd-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="822bd-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="822bd-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="822bd-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="822bd-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="822bd-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="822bd-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="822bd-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="822bd-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="822bd-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="822bd-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

