---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424118"
---
# <a name="mapilogonex"></a><span data-ttu-id="bb7c3-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="bb7c3-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="bb7c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb7c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb7c3-105">Connecte une application cliente à une session avec le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb7c3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bb7c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb7c3-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="bb7c3-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="bb7c3-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bb7c3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bb7c3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bb7c3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bb7c3-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bb7c3-110">Called by:</span></span>  <br/> |<span data-ttu-id="bb7c3-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="bb7c3-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="bb7c3-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="bb7c3-112">Parameters</span></span>

 <span data-ttu-id="bb7c3-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bb7c3-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="bb7c3-114">[in] Handle vers la fenêtre à laquelle la boîte de dialogue d’ouverture de conversation est modale.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="bb7c3-115">Si aucune boîte de dialogue n’apparaît pendant l’appel, le  _paramètre ulUIParam_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="bb7c3-116">Ce paramètre peut être zéro.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="bb7c3-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="bb7c3-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="bb7c3-118">[in] Pointeur vers une chaîne qui contient le nom du profil à utiliser lorsque l’utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="bb7c3-119">Cette chaîne est limitée à 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="bb7c3-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="bb7c3-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="bb7c3-121">[in] Pointeur vers une chaîne qui contient le mot de passe du profil.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="bb7c3-122">Le  _paramètre lpszPassword_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="bb7c3-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="bb7c3-123">_flFlags_</span></span>
  
> <span data-ttu-id="bb7c3-124">[in] Masque de bits d’indicateurs utilisés pour contrôler l’utilisation de la logon.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="bb7c3-125">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="bb7c3-125">The following flags can be set:</span></span>
    
<span data-ttu-id="bb7c3-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="bb7c3-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="bb7c3-127">La session partagée doit être renvoyée, ce qui permet aux clients ultérieurs d’obtenir la session sans fournir d’informations d’identification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="bb7c3-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="bb7c3-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="bb7c3-129">Connectez-vous à une session et exécutez toutes les opérations en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="bb7c3-130">En règle générale, si un client a l’intention de traiter sur un thread d’arrière-plan ou dans un processus distinct d’une manière qui n’est pas discrète du thread au premier plan, il doit appeler avec l’indicateur MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="bb7c3-131">Une application cliente telle qu’un moteur d’indexation ou l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès au type en arrière-plan sont quelques exemples d’utilisation de MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="bb7c3-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="bb7c3-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="bb7c3-133">Le profil par défaut ne doit pas être utilisé et l’utilisateur doit être tenu de fournir un profil.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="bb7c3-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="bb7c3-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="bb7c3-135">Connectez-vous avec des fonctionnalités étendues.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-135">Log on with extended capabilities.</span></span> <span data-ttu-id="bb7c3-136">Cet indicateur doit toujours être définie.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-136">This flag should always be set.</span></span>
    
<span data-ttu-id="bb7c3-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="bb7c3-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="bb7c3-138">Une tentative de téléchargement de tous les messages de l’utilisateur doit être réalisée avant de revenir.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="bb7c3-139">Si l MAPI_FORCE_DOWNLOAD n’est pas définie, les messages peuvent être téléchargés en arrière-plan après le retour de l’appel à MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="bb7c3-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="bb7c3-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="bb7c3-141">Une boîte de dialogue doit s’afficher pour permettre à l’utilisateur d’obtenir des informations d’accès si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="bb7c3-142">Lorsque l’indicateur MAPI_LOGON_UI n’est pas définie, le client appelant n’affiche pas de boîte de dialogue de session et renvoie une valeur d’erreur si l’utilisateur n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="bb7c3-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="bb7c3-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="bb7c3-144">Une tentative doit être réalisée pour créer une nouvelle session MAPI au lieu d’acquérir la session partagée.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="bb7c3-145">Si l MAPI_NEW_SESSION n’est pas définie, MAPILogonEx utilise une session partagée existante, même si le paramètre  _lpszprofileName_ n’est pas NULL.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="bb7c3-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="bb7c3-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="bb7c3-147">MAPI ne doit pas informer lepooler MAPI de l’existence de la session.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="bb7c3-148">Le résultat est qu’aucun message ne peut être envoyé ou reçu dans la session, sauf par le biais d’une paire de transport et de magasin étroitement couplée.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="bb7c3-149">Un client appelant définit cet indicateur s’il agit en tant qu’agent, si un travail de configuration doit être effectué ou si le client parcourant les magasins de messages disponibles.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="bb7c3-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="bb7c3-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="bb7c3-151">L’appelant est en cours d’exécution en tant Windows service.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="bb7c3-152">Les appelants qui ne s’exécutent pas en tant que service Windows ne doivent pas définir cet indicateur . les appelants qui s’exécutent en tant que service doivent définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="bb7c3-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="bb7c3-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="bb7c3-154">MAPILogonEx doit afficher une boîte de dialogue de configuration pour chaque service de message dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="bb7c3-155">Les boîtes de dialogue s’affichent une fois que le profil a été choisi, mais avant qu’un service de message ne soit connecté.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="bb7c3-156">La boîte de dialogue COMMUNE MAPI pour l’ouverture de conversation contient également une case à cocher qui demande la même opération.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="bb7c3-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="bb7c3-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="bb7c3-158">L’accès doit échouer s’il est bloqué pendant plus de quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="bb7c3-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb7c3-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bb7c3-160">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="bb7c3-161">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="bb7c3-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="bb7c3-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="bb7c3-163">Le sous-système de messagerie doit remplacer le nom de profil du profil par défaut par le paramètre _lpszProfileName._</span><span class="sxs-lookup"><span data-stu-id="bb7c3-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="bb7c3-164">L MAPI_EXPLICIT_PROFILE est ignoré, sauf  _si lpszProfileName_ est NULL ou vide.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="bb7c3-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="bb7c3-165">_lppSession_</span></span>
  
> <span data-ttu-id="bb7c3-166">[out] Pointeur vers un pointeur vers l’interface de session MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb7c3-167">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb7c3-167">Return value</span></span>

<span data-ttu-id="bb7c3-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb7c3-168">S_OK</span></span> 
  
> <span data-ttu-id="bb7c3-169">L’logo a réussi.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-169">The logon succeeded.</span></span>
    
<span data-ttu-id="bb7c3-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="bb7c3-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="bb7c3-171">L’ouverture de session a échoué, soit parce qu’un ou plusieurs des paramètres de MAPILogonEx n’étaient pas valides, soit parce qu’il y avait déjà trop de sessions ouvertes.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="bb7c3-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bb7c3-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="bb7c3-173">MAPI sérialise toutes les connexions via un mutex.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="bb7c3-174">Elle est renvoyée si l’MAPI_TIMEOUT_SHORT a été définie et qu’un autre thread a tenu le mutex.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="bb7c3-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bb7c3-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="bb7c3-176">L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bb7c3-177">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb7c3-177">Remarks</span></span>

<span data-ttu-id="bb7c3-178">Les applications clientes MAPI appellent la fonction MAPILogonEx pour se connecter à une session avec le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="bb7c3-179">Toutes les chaînes transmises et renvoyées à et à partir d’appels MAPI sont terminées par null et doivent être spécifiées dans le jeu de caractères ou la page de code actuel du système d’exploitation du client ou du fournisseur appelant.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="bb7c3-180">Le  _paramètre lpszProfileName_ est ignoré s’il existe une session précédente qui a appelé MapiLogonEx avec l’indicateur MAPI_ALLOW_OTHERS et si l’indicateur MAPI_NEW_SESSION n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="bb7c3-181">Si le paramètre  _lpszProfileName_ est NULL ou pointe vers une chaîne vide, et que le paramètre  _flFlags_ inclut l’indicateur MAPI_LOGON_UI, la fonction MAPILogonEx génère une boîte de dialogue d’accès avec un champ vide pour le nom de profil.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="bb7c3-182">Lors de la connexion à un profil spécifique, un client doit transmettre l’indicateur MAPI_NEW_SESSION mapiLogonEx en plus du nom de profil.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="bb7c3-183">Dans le cas contraire, si un autre client a établi une session partagée en se connectant avec MAPI_ALLOW_OTHERS, le client est connecté à la session partagée au lieu du profil demandé.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="bb7c3-184">L MAPI_EXPLICIT_PROFILE ne provoque pas l’utilisation du nom de profil par défaut lorsque  _lpszProfileName_ est NULL ou vide, sauf si l’indicateur MAPI_USE_DEFAULT est également présent.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="bb7c3-185">L MAPI_NO_MAIL’indicateur a plusieurs effets qui provoquent les effets suivants lorsque vous n’utilisez pas lepooler MAPI :</span><span class="sxs-lookup"><span data-stu-id="bb7c3-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="bb7c3-186">Aucun message ne peut être envoyé ou remis par lepooler MAPI au cours de cette session.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="bb7c3-187">Seuls les fournisseurs de transport et de magasin étroitement couplés peuvent envoyer et remettre des messages.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="bb7c3-188">Les magasins basés sur un serveur peuvent toujours envoyer ou remettre des messages.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="bb7c3-189">Les messages envoyés ou remis par des magasins basés sur le serveur ne sont pas traitées par des fournisseurs de crochets.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="bb7c3-190">Les options de transport par message et par destinataire ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="bb7c3-191">La table d’état ne contient pas d’entrées pour les fournisseurs de transport et aucune fonctionnalité de transport dépendante des objets d’état (tels que la configuration) n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="bb7c3-192">La ligne dupooler de message dans la table d’état contient la STATUS_FAILURE valeur.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="bb7c3-193">Les connexions pibacked sont autorisées, mais ces connexions n’entraînent pas la réception des mises à jour de l’objet d’état par la connexion précédente.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="bb7c3-194">Un service doit toujours se connecter à l’aide de l MAPI_NO_MAIL de connexion.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb7c3-195">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bb7c3-195">MFCMAPI reference</span></span>

<span data-ttu-id="bb7c3-196">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb7c3-197">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="bb7c3-197">**File**</span></span>|<span data-ttu-id="bb7c3-198">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="bb7c3-198">**Function**</span></span>|<span data-ttu-id="bb7c3-199">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="bb7c3-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb7c3-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="bb7c3-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="bb7c3-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="bb7c3-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="bb7c3-202">MFCMAPI utilise la méthode MAPILogonEx pour se connecter à MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb7c3-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb7c3-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb7c3-203">See also</span></span>



[<span data-ttu-id="bb7c3-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="bb7c3-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="bb7c3-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="bb7c3-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="bb7c3-206">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="bb7c3-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

