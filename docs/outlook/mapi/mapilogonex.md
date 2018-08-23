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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: db76dfec27100a22785082580da70ecc2c10fc45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579983"
---
# <a name="mapilogonex"></a><span data-ttu-id="350ad-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="350ad-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="350ad-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="350ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="350ad-105">Enregistre une application client à une session avec le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="350ad-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="350ad-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="350ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="350ad-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="350ad-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="350ad-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="350ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="350ad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="350ad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="350ad-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="350ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="350ad-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="350ad-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="350ad-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="350ad-112">Parameters</span></span>

 <span data-ttu-id="350ad-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="350ad-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="350ad-114">[in] Handle vers la fenêtre à laquelle la boîte de dialogue d’ouverture de session est modale.</span><span class="sxs-lookup"><span data-stu-id="350ad-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="350ad-115">Si aucune boîte de dialogue s’affiche lors de l’appel, le paramètre _ulUIParam_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="350ad-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="350ad-116">Ce paramètre peut être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="350ad-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="350ad-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="350ad-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="350ad-118">[in] Pointeur vers une chaîne qui contient le nom du profil à utiliser lors de l’utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="350ad-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="350ad-119">Cette chaîne est limitée à 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="350ad-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="350ad-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="350ad-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="350ad-121">[in] Pointeur vers une chaîne qui contient le mot de passe du profil.</span><span class="sxs-lookup"><span data-stu-id="350ad-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="350ad-122">Le paramètre _lpszPassword_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="350ad-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="350ad-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="350ad-123">_flFlags_</span></span>
  
> <span data-ttu-id="350ad-124">[in] Masque de bits d’indicateurs utilisés pour contrôler la façon dont l’ouverture de session est effectuée.</span><span class="sxs-lookup"><span data-stu-id="350ad-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="350ad-125">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="350ad-125">The following flags can be set:</span></span>
    
<span data-ttu-id="350ad-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="350ad-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="350ad-127">La session partagée doit être retournée, qui permet une version ultérieure aux clients d’obtenir la session sans fournir les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="350ad-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="350ad-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="350ad-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="350ad-129">Ouvrez une session et exécuter des opérations en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="350ad-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="350ad-130">En règle générale, si un client a l’intention d’effectuer un traitement sur une thread d’arrière-plan ou dans un processus distinct d’une manière discrète à la thread de premier plan, il doit appeler avec l’indicateur MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="350ad-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="350ad-131">Une application cliente comme un moteur d’indexation ou de l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès de type d’arrière-plan sont des exemples d’utilisation de MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="350ad-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="350ad-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="350ad-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="350ad-133">Le profil par défaut ne doit pas être utilisé et que l’utilisateur doit être nécessaire de fournir un profil.</span><span class="sxs-lookup"><span data-stu-id="350ad-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="350ad-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="350ad-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="350ad-135">Ouvrez une session avec des capacités étendues.</span><span class="sxs-lookup"><span data-stu-id="350ad-135">Log on with extended capabilities.</span></span> <span data-ttu-id="350ad-136">Cet indicateur doit toujours être défini.</span><span class="sxs-lookup"><span data-stu-id="350ad-136">This flag should always be set.</span></span>
    
<span data-ttu-id="350ad-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="350ad-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="350ad-138">Une tentative doit être effectuée pour télécharger tous les messages de l’utilisateur avant de renvoyer.</span><span class="sxs-lookup"><span data-stu-id="350ad-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="350ad-139">Si l’indicateur MAPI_FORCE_DOWNLOAD n’est pas définie, les messages peuvent être téléchargés en arrière-plan après l’appel à MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="350ad-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="350ad-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="350ad-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="350ad-141">Une boîte de dialogue doit être affichée pour demander à l’utilisateur pour les informations de connexion si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="350ad-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="350ad-142">Lorsque l’indicateur MAPI_LOGON_UI n’est pas défini, le client appelant n’affiche pas une boîte de dialogue d’ouverture de session et renvoie une valeur d’erreur si l’utilisateur n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="350ad-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="350ad-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="350ad-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="350ad-144">Une tentative doit être effectuée pour créer une nouvelle session MAPI au lieu de l’acquisition de la session partagée.</span><span class="sxs-lookup"><span data-stu-id="350ad-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="350ad-145">Si l’indicateur MAPI_NEW_SESSION n’est pas définie, MAPILogonEx utilise une session partagée, même si le paramètre _lpszprofileName_ n’est pas NULL.</span><span class="sxs-lookup"><span data-stu-id="350ad-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="350ad-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="350ad-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="350ad-147">MAPI ne doit pas informer le spouleur MAPI de l’existence de la session.</span><span class="sxs-lookup"><span data-stu-id="350ad-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="350ad-148">Le résultat est qu’aucun message peut être envoyé ou reçu dans la session sauf via étroitement couplés stocker et paire de transport.</span><span class="sxs-lookup"><span data-stu-id="350ad-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="350ad-149">Un client appelant définit cet indicateur si elle agit comme un agent, si le travail de configuration doit être effectuée, ou si le client parcourt les banques de messages disponibles.</span><span class="sxs-lookup"><span data-stu-id="350ad-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="350ad-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="350ad-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="350ad-151">L’appelant est exécuté comme un service Windows.</span><span class="sxs-lookup"><span data-stu-id="350ad-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="350ad-152">Appelants qui n’exécutent pas comme un service Windows ne doit pas définir cet indicateur ; Cet indicateur doivent être défini par les appelants qui sont en cours d’exécution en tant que service.</span><span class="sxs-lookup"><span data-stu-id="350ad-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="350ad-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="350ad-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="350ad-154">MAPILogonEx doit afficher une boîte de dialogue de configuration pour chaque service de message dans le profil.</span><span class="sxs-lookup"><span data-stu-id="350ad-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="350ad-155">Les boîtes de dialogue sont affichent une fois que le profil a été sélectionné mais avant tout message service est connecté.</span><span class="sxs-lookup"><span data-stu-id="350ad-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="350ad-156">La boîte de dialogue commune MAPI pour l’ouverture de session contient également une case à cocher qui demande la même opération.</span><span class="sxs-lookup"><span data-stu-id="350ad-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="350ad-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="350ad-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="350ad-158">L’ouverture de session doit échouer si bloqué pendant plus de quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="350ad-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="350ad-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="350ad-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="350ad-160">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="350ad-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="350ad-161">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="350ad-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="350ad-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="350ad-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="350ad-163">Le sous-système de messagerie doit remplacer le nom de profil du profil par défaut pour le paramètre _lpszProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="350ad-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="350ad-164">L’indicateur MAPI_EXPLICIT_PROFILE est ignoré à moins que _lpszProfileName_ est NULL ou vide.</span><span class="sxs-lookup"><span data-stu-id="350ad-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="350ad-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="350ad-165">_lppSession_</span></span>
  
> <span data-ttu-id="350ad-166">[out] Pointeur vers un pointeur vers l’interface de session MAPI.</span><span class="sxs-lookup"><span data-stu-id="350ad-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="350ad-167">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="350ad-167">Return value</span></span>

<span data-ttu-id="350ad-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="350ad-168">S_OK</span></span> 
  
> <span data-ttu-id="350ad-169">La connexion a réussi.</span><span class="sxs-lookup"><span data-stu-id="350ad-169">The logon succeeded.</span></span>
    
<span data-ttu-id="350ad-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="350ad-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="350ad-171">La connexion a échoué, car un ou plusieurs des paramètres MAPILogonEx ne sont pas valides ou trop de sessions étaient déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="350ad-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="350ad-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="350ad-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="350ad-173">MAPI sérialise toutes les ouvertures de session via un mutex.</span><span class="sxs-lookup"><span data-stu-id="350ad-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="350ad-174">Il est renvoyé si l’indicateur MAPI_TIMEOUT_SHORT a été défini et un autre thread détenus mutex.</span><span class="sxs-lookup"><span data-stu-id="350ad-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="350ad-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="350ad-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="350ad-176">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="350ad-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="350ad-177">Remarques</span><span class="sxs-lookup"><span data-stu-id="350ad-177">Remarks</span></span>

<span data-ttu-id="350ad-178">Les applications clientes MAPI appellent la fonction MAPILogonEx pour vous connecter à une session avec le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="350ad-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="350ad-179">Toutes les chaînes qui sont transmis et renvoyés vers et depuis les appels MAPI sont terminée et doivent être spécifiés dans le jeu de caractères en cours ou page du système d’exploitation client ou du fournisseur d’appel de code.</span><span class="sxs-lookup"><span data-stu-id="350ad-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="350ad-180">Le paramètre _lpszProfileName_ est ignoré s’il existe une session précédente existante qui a appelé MapiLogonEx avec l’indicateur MAPI_ALLOW_OTHERS et si l’indicateur MAPI_NEW_SESSION n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="350ad-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="350ad-181">Si le paramètre _lpszProfileName_ est NULL ou pointe vers une chaîne vide et le paramètre _flFlags_ inclut l’indicateur MAPI_LOGON_UI, la fonction MAPILogonEx génère une boîte de dialogue d’ouverture de session qui a un champ vide pour le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="350ad-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="350ad-182">Lors de la connexion à un profil spécifique, un client doit passer l’indicateur MAPI_NEW_SESSION dans MAPILogonEx en plus du nom du profil.</span><span class="sxs-lookup"><span data-stu-id="350ad-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="350ad-183">Dans le cas contraire, si un autre client a établi une session partagée en vous connectant avec MAPI_ALLOW_OTHERS, le client sera connecté en à la session partagée au lieu d’au profil demandé.</span><span class="sxs-lookup"><span data-stu-id="350ad-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="350ad-184">L’indicateur MAPI_EXPLICIT_PROFILE pas provoquer le nom du profil par défaut à utiliser lorsque _lpszProfileName_ a la valeur NULL est vide ou ne, sauf si l’indicateur MAPI_USE_DEFAULT est également présent.</span><span class="sxs-lookup"><span data-stu-id="350ad-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="350ad-185">L’indicateur MAPI_NO_MAIL a plusieurs effets provoquer ce qui suit lorsque vous n’utilisez ne pas le spouleur MAPI :</span><span class="sxs-lookup"><span data-stu-id="350ad-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="350ad-186">Aucun message ne peut être envoyées ou transmis par le spouleur MAPI pendant cette session.</span><span class="sxs-lookup"><span data-stu-id="350ad-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="350ad-187">Seuls fournisseurs de banque et de transport étroitement couplés peuvent envoyer et remettre des messages.</span><span class="sxs-lookup"><span data-stu-id="350ad-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="350ad-188">Magasins de serveur peuvent toujours envoyer ou remettre des messages.</span><span class="sxs-lookup"><span data-stu-id="350ad-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="350ad-189">Messages envoyés et remis par les magasins de serveur ne sont pas traitées par les fournisseurs de raccordement.</span><span class="sxs-lookup"><span data-stu-id="350ad-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="350ad-190">Options de chaque message et par destinataire pour des transports ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="350ad-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="350ad-191">La table d’état ne contient-elle pas d’entrées pour les fournisseurs de transport et les fonctionnalités de transport dépendent d’objets d’état (par exemple, configuration) ne sont pas disponible.</span><span class="sxs-lookup"><span data-stu-id="350ad-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="350ad-192">La ligne dans la table d’état spouleur du message contient la valeur de la valeur.</span><span class="sxs-lookup"><span data-stu-id="350ad-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="350ad-193">Ouvertures de session superposables (piggyback) sont autorisés, mais les ouvertures de session ne provoquent pas l’ouverture de session précédente recevoir des mises à jour de statut objet.</span><span class="sxs-lookup"><span data-stu-id="350ad-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="350ad-194">Un service doit toujours se connecter à l’aide de l’indicateur MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="350ad-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="350ad-195">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="350ad-195">MFCMAPI reference</span></span>

<span data-ttu-id="350ad-196">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="350ad-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="350ad-197">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="350ad-197">**File**</span></span>|<span data-ttu-id="350ad-198">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="350ad-198">**Function**</span></span>|<span data-ttu-id="350ad-199">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="350ad-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="350ad-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="350ad-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="350ad-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="350ad-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="350ad-202">MFCMAPI utilise la méthode MAPILogonEx pour se connecter à MAPI.</span><span class="sxs-lookup"><span data-stu-id="350ad-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="350ad-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="350ad-203">See also</span></span>



[<span data-ttu-id="350ad-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="350ad-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="350ad-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="350ad-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="350ad-206">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="350ad-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

