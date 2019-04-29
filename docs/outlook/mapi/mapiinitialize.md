---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411175"
---
# <a name="mapiinitialize"></a><span data-ttu-id="abf81-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="abf81-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="abf81-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abf81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abf81-105">Incrémente le nombre de références du sous-système MAPI et initialise les données globales pour la DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="abf81-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abf81-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="abf81-106">Header file:</span></span>  <br/> |<span data-ttu-id="abf81-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="abf81-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="abf81-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="abf81-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="abf81-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="abf81-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="abf81-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="abf81-110">Called by:</span></span>  <br/> |<span data-ttu-id="abf81-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="abf81-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="abf81-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abf81-112">Parameters</span></span>

 <span data-ttu-id="abf81-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="abf81-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="abf81-114">dans Pointeur vers une structure [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="abf81-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="abf81-115">Le paramètre _lpMapiInit_ peut être défini sur null.</span><span class="sxs-lookup"><span data-stu-id="abf81-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="abf81-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="abf81-116">Return value</span></span>

<span data-ttu-id="abf81-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="abf81-117">S_OK</span></span> 
  
> <span data-ttu-id="abf81-118">Le sous-système MAPI a été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="abf81-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abf81-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="abf81-119">Remarks</span></span>

<span data-ttu-id="abf81-120">La fonction **MAPIInitialize** incrémente le nombre de références MAPI pour le sous-système MAPI et la fonction [MAPIUninitialize](mapiuninitialize.md) décrémente le nombre de références internes.</span><span class="sxs-lookup"><span data-stu-id="abf81-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="abf81-121">Par conséquent, le nombre d'appels à une fonction doit être égal au nombre d'appels à l'autre.</span><span class="sxs-lookup"><span data-stu-id="abf81-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="abf81-122">**MAPIInitialize** renvoie S_OK si MAPI n'a pas été précédemment initialisé.</span><span class="sxs-lookup"><span data-stu-id="abf81-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="abf81-123">Un client ou un fournisseur de services doit appeler **MAPIInitialize** avant d'établir tout autre appel MAPI.</span><span class="sxs-lookup"><span data-stu-id="abf81-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="abf81-124">Si ce n'est pas le cas, les appels du client ou du fournisseur de services renvoient la valeur MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="abf81-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="abf81-125">Lors de l'appel de **MAPIInitialize** à partir d'une application multithread, définissez le paramètre _lpMapiInit_ sur une structure [MAPIINIT_0](mapiinit_0.md) qui est déclarée comme suit:</span><span class="sxs-lookup"><span data-stu-id="abf81-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="abf81-126">**MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="abf81-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="abf81-127">et appelez:</span><span class="sxs-lookup"><span data-stu-id="abf81-127">and call:</span></span> 
  
 <span data-ttu-id="abf81-128">**MAPIInitialize** (&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="abf81-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="abf81-129">Lorsque cette structure est déclarée, MAPI crée un thread distinct pour gérer la fenêtre de notification, qui continue jusqu'à ce que le nombre de références d'initialisation tombe à zéro.</span><span class="sxs-lookup"><span data-stu-id="abf81-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="abf81-130">Un service Windows doit définir le membre **ulflags** de la structure **MAPIINIT_0** vers laquelle pointe _lpMapiInit_ vers MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="abf81-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="abf81-131">Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d'une fonction **DllMain** Win32 ou de toute autre fonction qui crée ou termine des threads.</span><span class="sxs-lookup"><span data-stu-id="abf81-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="abf81-132">Pour plus d'informations, consultez la rubrique [utilisation d'objets thread-safe](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="abf81-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="abf81-133">**MAPIInitialize** ne renvoie aucune information d'erreur étendue.</span><span class="sxs-lookup"><span data-stu-id="abf81-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="abf81-134">Contrairement à la plupart des autres appels MAPI, la signification de ses valeurs de retour est strictement définie pour correspondre à l'étape particulière de l'initialisation qui a échoué:</span><span class="sxs-lookup"><span data-stu-id="abf81-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="abf81-135">Vérifie les paramètres et les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="abf81-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="abf81-136">MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="abf81-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="abf81-137">L'appelant a passé un paramètre ou un indicateur non valide.</span><span class="sxs-lookup"><span data-stu-id="abf81-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="abf81-138">Initialise les clés de Registre requises par MAPI et confirme le type de système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="abf81-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="abf81-139">Cette étape se produit uniquement si le processus client est exécuté en tant que service sous Windows et définit l'indicateur de SERVICE MAPI_NT dans la structure **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="abf81-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="abf81-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="abf81-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="abf81-141">Le processus appelant est un service Windows et les clés de Registre requises par MAPI n'ont pas pu être initialisées.</span><span class="sxs-lookup"><span data-stu-id="abf81-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="abf81-142">Des informations supplémentaires peuvent être disponibles dans le journal des événements d'application.</span><span class="sxs-lookup"><span data-stu-id="abf81-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="abf81-143">Vérifiez la compatibilité de MAPI avec OLE, puis initialisez OLE.</span><span class="sxs-lookup"><span data-stu-id="abf81-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="abf81-144">Vérifie la compatibilité entre les versions actuelles d'OLE et MAPI.</span><span class="sxs-lookup"><span data-stu-id="abf81-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="abf81-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="abf81-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="abf81-146">La version d'OLE installée sur la station de travail n'est pas compatible avec cette version de MAPI.</span><span class="sxs-lookup"><span data-stu-id="abf81-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="abf81-147">Initialise OLE.</span><span class="sxs-lookup"><span data-stu-id="abf81-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="abf81-148">Au cours de cette étape uniquement, cette fonction peut renvoyer un code d'erreur non répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="abf81-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="abf81-149">Toute erreur _non_ répertoriée ici doit être supposée provenir de la **CoInitialize**de la fonction OLE.</span><span class="sxs-lookup"><span data-stu-id="abf81-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="abf81-150">Initialise les variables globales par processus.</span><span class="sxs-lookup"><span data-stu-id="abf81-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="abf81-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="abf81-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="abf81-152">MAPI définit le contexte spécifique au processus actuel.</span><span class="sxs-lookup"><span data-stu-id="abf81-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="abf81-153">Des échecs peuvent se produire sur Win16 si le nombre de processus dépasse un certain nombre ou sur n'importe quel système si la mémoire disponible est épuisée.</span><span class="sxs-lookup"><span data-stu-id="abf81-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="abf81-154">Initialise les variables globales partagées de tous les processus.</span><span class="sxs-lookup"><span data-stu-id="abf81-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="abf81-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="abf81-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="abf81-156">Les ressources système disponibles sont insuffisantes pour terminer l'opération.</span><span class="sxs-lookup"><span data-stu-id="abf81-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="abf81-157">Initialise le moteur de notification, crée sa fenêtre et son thread s'il est demandé par l'indicateur MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="abf81-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="abf81-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="abf81-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="abf81-159">Peut échouer si les ressources système sont épuisées.</span><span class="sxs-lookup"><span data-stu-id="abf81-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="abf81-160">Charge et initialise le fournisseur de profils.</span><span class="sxs-lookup"><span data-stu-id="abf81-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="abf81-161">Vérifie que **MAPIInitialize** peut accéder à la clé de registre où sont stockées les données de profil.</span><span class="sxs-lookup"><span data-stu-id="abf81-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="abf81-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="abf81-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="abf81-163">Le fournisseur de profils a rencontré une erreur.</span><span class="sxs-lookup"><span data-stu-id="abf81-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="abf81-164">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="abf81-164">MFCMAPI reference</span></span>

<span data-ttu-id="abf81-165">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="abf81-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="abf81-166">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="abf81-166">**File**</span></span>|<span data-ttu-id="abf81-167">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="abf81-167">**Function**</span></span>|<span data-ttu-id="abf81-168">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="abf81-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="abf81-169">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="abf81-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="abf81-170">MFCMAPI utilise la méthode **MAPIInitialize** pour initialiser MAPI sur un thread d'arrière-plan pour effectuer un traitement de table.</span><span class="sxs-lookup"><span data-stu-id="abf81-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abf81-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abf81-171">See also</span></span>



[<span data-ttu-id="abf81-172">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="abf81-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

