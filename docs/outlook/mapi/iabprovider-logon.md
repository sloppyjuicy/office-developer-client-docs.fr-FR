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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 21a6907f7511779d7e8ec6825ac68d109d2f48eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783606"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="b65d0-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="b65d0-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="b65d0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b65d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b65d0-105">Établit une connexion à une session active.</span><span class="sxs-lookup"><span data-stu-id="b65d0-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b65d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b65d0-106">Parameters</span></span>

 <span data-ttu-id="b65d0-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="b65d0-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="b65d0-108">[in] Pointeur vers l’objet de prise en charge du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b65d0-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="b65d0-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b65d0-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="b65d0-110">[in] Handle vers la fenêtre parente de la boîte de dialogue d’ouverture de session qui affiche la méthode **d’ouverture de session** , en cas d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="b65d0-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="b65d0-111">Le paramètre _ulUIParam_ contient la valeur du paramètre du même nom passé à MAPI dans l’appel à la fonction [MAPILogonEx](mapilogonex.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="b65d0-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="b65d0-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="b65d0-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="b65d0-113">[in] Pointeur vers le nom du profil de la session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="b65d0-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b65d0-114">_ulFlags_</span></span>
  
> <span data-ttu-id="b65d0-115">[in] Masque de bits d’indicateurs qui contrôle la façon dont les paramètres de connexion est effectuée.</span><span class="sxs-lookup"><span data-stu-id="b65d0-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="b65d0-116">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="b65d0-116">The following flags can be set:</span></span>
    
<span data-ttu-id="b65d0-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b65d0-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="b65d0-118">Le fournisseur ne doit pas afficher une boîte de dialogue au cours de l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="b65d0-119">Si cet indicateur n’est pas défini, le fournisseur peut afficher une boîte de dialogue pour inviter l’utilisateur pour les informations de configuration manquantes.</span><span class="sxs-lookup"><span data-stu-id="b65d0-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="b65d0-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b65d0-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b65d0-121">Permet l' **ouverture de session** renvoyer avec succès, éventuellement, avant l’ouverture de session est terminée.</span><span class="sxs-lookup"><span data-stu-id="b65d0-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="b65d0-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b65d0-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b65d0-123">Toutes les chaînes doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="b65d0-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="b65d0-124">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="b65d0-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="b65d0-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="b65d0-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="b65d0-126">[entrée, sortie] Un pointeur vers la taille, en octets, de la structure d’informations d’identification de sécurité indiqué par le paramètre _lppbSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="b65d0-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="b65d0-127">À l’entrée, la valeur doit être différente de zéro ; dans la sortie, la valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b65d0-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="b65d0-128">Dans les deux cas, les pointeurs doivent être valides.</span><span class="sxs-lookup"><span data-stu-id="b65d0-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="b65d0-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="b65d0-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="b65d0-130">[entrée, sortie] Pointeur vers un pointeur vers les informations d’identification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b65d0-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="b65d0-131">À l’entrée, la valeur doit être différente de zéro ; dans la sortie, la valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b65d0-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="b65d0-132">Dans les deux cas, le pointeur doit être valid.</span><span class="sxs-lookup"><span data-stu-id="b65d0-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="b65d0-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b65d0-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b65d0-134">[out] Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="b65d0-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="b65d0-135">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer.</span><span class="sxs-lookup"><span data-stu-id="b65d0-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="b65d0-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="b65d0-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="b65d0-137">[out] Pointeur vers un pointeur vers l’objet du fournisseur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b65d0-138">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b65d0-138">Return value</span></span>

<span data-ttu-id="b65d0-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="b65d0-139">S_OK</span></span> 
  
> <span data-ttu-id="b65d0-140">Une connexion à une session active a été établie.</span><span class="sxs-lookup"><span data-stu-id="b65d0-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="b65d0-141">RÉFÉRENCE À MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="b65d0-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="b65d0-142">Le fournisseur ne peut pas se connecter, mais MAPI peut continuer à se connecter sur les autres fournisseurs dans le service de message à laquelle appartient le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="b65d0-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="b65d0-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="b65d0-144">Le fournisseur n’a pas suffisamment d’informations pour effectuer l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="b65d0-145">MAPI appelle la fonction de l’entrée de service de message du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="b65d0-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="b65d0-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="b65d0-147">Le serveur n’est pas configuré pour prendre en charge de la page de codes du client.</span><span class="sxs-lookup"><span data-stu-id="b65d0-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="b65d0-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="b65d0-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="b65d0-149">Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.</span><span class="sxs-lookup"><span data-stu-id="b65d0-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="b65d0-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b65d0-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b65d0-151">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b65d0-152">Remarques</span><span class="sxs-lookup"><span data-stu-id="b65d0-152">Remarks</span></span>

<span data-ttu-id="b65d0-153">Connexions sont établies avec chaque fournisseur de carnet d’adresses dans le profil de session lorsqu’un client appelle la méthode [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) .</span><span class="sxs-lookup"><span data-stu-id="b65d0-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="b65d0-154">**OpenAddressBook** appelle ensuite la méthode **d’ouverture de session** de chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="b65d0-155">Le nom de profil vers laquelle pointé le paramètre _lpszProfileName_ s’affiche dans le jeu de caractères du client de l’utilisateur comme indiqué par la présence ou l’absence de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b65d0-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b65d0-156">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b65d0-156">Notes to implementers</span></span>

<span data-ttu-id="b65d0-157">Dans votre implémentation de la méthode **d’ouverture de session** , appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire un identificateur unique, ou une structure [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="b65d0-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="b65d0-158">Chacun de vos objets aura un identificateur d’entrée qui inclut ce **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="b65d0-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="b65d0-159">MAPI utilise le **MAPIUID** pour correspondre à un objet avec son fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="b65d0-160">Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un utilisateur de messagerie, **OpenEntry** examine la partie **MAPIUID** de l’identificateur d’entrée qui a été passé et qu’il correspond à un **MAPIUID** enregistrés en une fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b65d0-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="b65d0-161">Si un client se connecte à votre fournisseur plusieurs fois, vous souhaiterez peut-être inscrire un autre **MAPIUID** pour chaque ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="b65d0-162">Inscription des structures **MAPIUID** uniques permet de MAPI router correctement les demandes à l’instance de fournisseur approprié.</span><span class="sxs-lookup"><span data-stu-id="b65d0-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="b65d0-163">Toutefois, vous souhaiterez peut-être ont tous les objets d’ouverture de session de partager un **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="b65d0-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="b65d0-164">Dans ce cas, vous devez être en mesure de gérer le routage vous-même au lieu de s’appuyer sur MAPI.</span><span class="sxs-lookup"><span data-stu-id="b65d0-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="b65d0-165">Pour plus d’informations sur la création d’un **MAPIUID**, voir [Inscription des identificateurs uniques Service fournisseur](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b65d0-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="b65d0-166">L’objet de prise en charge MAPI transmet à votre méthode **d’ouverture de session** dans le paramètre _lpMAPISup_ fournit l’accès à de nombreuses méthodes inclus dans le [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="b65d0-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="b65d0-167">MAPI crée un objet de prise en charge qui est adapté à votre type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="b65d0-168">Par exemple, si vous avez besoin pour vous connecter à un système de messagerie sous-jacent ou le service d’annuaire lorsque vous établissez une connexion, vous pouvez appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour récupérer les informations d’identification de sécurité pour cette session particulière.</span><span class="sxs-lookup"><span data-stu-id="b65d0-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="b65d0-169">Si **l’ouverture de session** réussit, assurez-vous que vous appelez la méthode [IUnknown::AddRef](http://msdn.microsoft.com/fr-fr/library/ms691379%28VS.85%29.aspx) de l’objet de la prise en charge pour incrémenter son décompte de références.</span><span class="sxs-lookup"><span data-stu-id="b65d0-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](http://msdn.microsoft.com/fr-fr/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="b65d0-170">Cela permet à votre fournisseur de conserver le pointeur d’objet prise en charge pour le reste de la session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="b65d0-171">Si vous n’appelez pas cette méthode **AddRef** , MAPI décharge votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="b65d0-172">Vous pouvez inclure le nom de profil transmis dans le paramètre _lpszProfileName_ dans les boîtes de dialogue d’erreur, écrans d’ouverture de session ou autres interfaces utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="b65d0-173">Pour utiliser le nom de profil, copiez-le vers un stockage que vous avez alloué.</span><span class="sxs-lookup"><span data-stu-id="b65d0-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="b65d0-174">Créer un objet d’ouverture de session et d’y revenir un pointeur dans le paramètre _lppABLogon_ .</span><span class="sxs-lookup"><span data-stu-id="b65d0-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="b65d0-175">MAPI utilise cet objet d’ouverture de session pour effectuer des appels aux méthodes dans votre implémentation [IABLogon](iablogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="b65d0-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="b65d0-176">Si vous avez besoin d’un mot de passe au cours de l’ouverture de session, afficher une boîte de dialogue d’ouverture de session uniquement si l’indicateur AB_NO_DIALOG n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="b65d0-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="b65d0-177">Si l’utilisateur annule le processus d’ouverture de session, généralement retourner MAPI_E_USER_CANCEL en cliquant sur le bouton **Annuler** dans la boîte de dialogue **d’ouverture de session**.</span><span class="sxs-lookup"><span data-stu-id="b65d0-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="b65d0-178">En règle générale, lorsqu’un fournisseur de carnet d’adresses ne peut pas se connecter, MAPI désactive le service de message à laquelle appartient le fournisseur défectueux — autrement dit, MAPI n’essaie pas d’établir des connexions pour tous les autres fournisseurs qui appartiennent au service pour le reste de la session durée de vie.</span><span class="sxs-lookup"><span data-stu-id="b65d0-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="b65d0-179">Cependant, si votre fournisseur ne peut pas établir une connexion et que vous souhaitez ne pas désactiver le service entier, renvoie une référence à MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="b65d0-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="b65d0-180">MAPI ne désactive pas le service de message à laquelle appartient le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="b65d0-181">Retour référence à MAPI_E_FAILONEPROVIDER si une erreur produit qui n’est pas suffisamment grave pour empêcher les autres fournisseurs dans le service de message d’établir des connexions.</span><span class="sxs-lookup"><span data-stu-id="b65d0-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="b65d0-182">Retourner MAPI_E_UNCONFIGURED si les informations de configuration nécessaires sont absents du profil et vous ne pouvez pas afficher une boîte de dialogue pour inviter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b65d0-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="b65d0-183">MAPI répond en fonction de point d’entrée de votre fournisseur message service MSG_SERVICE_CONFIGURE pourvue l’appel en tant que paramètre _ulContext_ pour donner la possibilité de configurer lui-même, soit par programme le service ou à l’aide d’une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b65d0-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="b65d0-184">Lorsque le message service point d’entrée fonction est terminé, MAPI réessayer l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b65d0-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b65d0-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b65d0-185">See also</span></span>



[<span data-ttu-id="b65d0-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="b65d0-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="b65d0-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b65d0-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="b65d0-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="b65d0-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="b65d0-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="b65d0-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="b65d0-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="b65d0-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="b65d0-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b65d0-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

