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
# <a name="mapiinitialize"></a><span data-ttu-id="603c5-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="603c5-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="603c5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="603c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="603c5-105">Incrémente le nombre de références du sous-système MAPI et initialise les données globales pour la DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="603c5-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="603c5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="603c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="603c5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="603c5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="603c5-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="603c5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="603c5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="603c5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="603c5-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="603c5-110">Called by:</span></span>  <br/> |<span data-ttu-id="603c5-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="603c5-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="603c5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="603c5-112">Parameters</span></span>

 <span data-ttu-id="603c5-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="603c5-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="603c5-114">[in] Pointeur vers une [MAPIINIT_0](mapiinit_0.md) structure.</span><span class="sxs-lookup"><span data-stu-id="603c5-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="603c5-115">Le  _paramètre lpMapiInit_ peut être définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="603c5-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="603c5-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="603c5-116">Return value</span></span>

<span data-ttu-id="603c5-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="603c5-117">S_OK</span></span> 
  
> <span data-ttu-id="603c5-118">Le sous-système MAPI a été initialisé avec succès.</span><span class="sxs-lookup"><span data-stu-id="603c5-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="603c5-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="603c5-119">Remarks</span></span>

<span data-ttu-id="603c5-120">La **fonction MAPIInitialize** incrémente le nombre de références MAPI pour le sous-système MAPI, et la fonction [MAPIUninitialize](mapiuninitialize.md) décrémente le nombre de références internes.</span><span class="sxs-lookup"><span data-stu-id="603c5-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="603c5-121">Par conséquent, le nombre d’appels à une fonction doit être égal au nombre d’appels à l’autre.</span><span class="sxs-lookup"><span data-stu-id="603c5-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="603c5-122">**MAPIInitialize** renvoie S_OK si MAPI n’a pas été initialisé précédemment.</span><span class="sxs-lookup"><span data-stu-id="603c5-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="603c5-123">Un client ou un fournisseur de services doit appeler **MAPIInitialize** avant d’effectuer tout autre appel MAPI.</span><span class="sxs-lookup"><span data-stu-id="603c5-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="603c5-124">Si vous ne le faites pas, les appels du client ou du fournisseur de services retournent la MAPI_E_NOT_INITIALIZED valeur.</span><span class="sxs-lookup"><span data-stu-id="603c5-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="603c5-125">Lorsque vous appelez **MAPIInitialize** à partir d’une application multithread, définissez le paramètre  _lpMapiInit_ sur une structure [MAPIINIT_0](mapiinit_0.md) déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="603c5-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="603c5-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="603c5-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="603c5-127">et appelez :</span><span class="sxs-lookup"><span data-stu-id="603c5-127">and call:</span></span> 
  
 <span data-ttu-id="603c5-128">**MAPIInitialize** ( &amp; MAPIINIT) ;</span><span class="sxs-lookup"><span data-stu-id="603c5-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="603c5-129">Lorsque cette structure est déclarée, MAPI crée un thread distinct pour gérer la fenêtre de notification, qui se poursuit jusqu’à ce que le nombre de références d’initialisation tombe à zéro.</span><span class="sxs-lookup"><span data-stu-id="603c5-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="603c5-130">Un service Windows doit définir le membre **lags** de la structure **MAPIINIT_0** pointée par  _lpMapiInit_ sur MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="603c5-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="603c5-131">Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d’une fonction **Win32 DllMain** ou toute autre fonction qui crée ou termine des threads.</span><span class="sxs-lookup"><span data-stu-id="603c5-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="603c5-132">Pour plus d’informations, [voir Using Thread-Safe Objects](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="603c5-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="603c5-133">**MAPIInitialize ne** retourne aucune information d’erreur étendue.</span><span class="sxs-lookup"><span data-stu-id="603c5-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="603c5-134">Contrairement à la plupart des autres appels MAPI, les significations de ses valeurs de retour sont strictement définies pour correspondre à l’étape particulière de l’initialisation qui a échoué :</span><span class="sxs-lookup"><span data-stu-id="603c5-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="603c5-135">Vérifie les paramètres et les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="603c5-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="603c5-136">MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="603c5-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="603c5-137">L’appelant a transmis un paramètre ou un indicateur non valide.</span><span class="sxs-lookup"><span data-stu-id="603c5-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="603c5-138">Initialise les clés de Registre requises par MAPI et confirme le type de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="603c5-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="603c5-139">Cette étape se produit uniquement si le processus client s’exécute en tant que service sous Windows et définit l’indicateur MAPI_NT SERVICE dans la structure **MAPIINIT_0** client.</span><span class="sxs-lookup"><span data-stu-id="603c5-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="603c5-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="603c5-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="603c5-141">Le processus d’appel est un service Windows et les clés de Registre requises par MAPI n’ont pas pu être initialisées.</span><span class="sxs-lookup"><span data-stu-id="603c5-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="603c5-142">Des informations supplémentaires peuvent être disponibles dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="603c5-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="603c5-143">Vérifiez la compatibilité de MAPI avec OLE, puis initialisez OLE.</span><span class="sxs-lookup"><span data-stu-id="603c5-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="603c5-144">Vérifie la compatibilité entre les versions actuelles de OLE et MAPI.</span><span class="sxs-lookup"><span data-stu-id="603c5-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="603c5-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="603c5-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="603c5-146">La version de OLE installée sur la station de travail n’est pas compatible avec cette version de MAPI.</span><span class="sxs-lookup"><span data-stu-id="603c5-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="603c5-147">Initialise OLE.</span><span class="sxs-lookup"><span data-stu-id="603c5-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="603c5-148">Au cours de cette étape uniquement, cette fonction peut renvoyer un code d’erreur non répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="603c5-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="603c5-149">Toute erreur  _non_ répertoriée ici doit être supposée être provenant de la fonction OLE **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="603c5-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="603c5-150">Initialise les variables globales par processus.</span><span class="sxs-lookup"><span data-stu-id="603c5-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="603c5-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="603c5-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="603c5-152">MAPI définit un contexte spécifique au processus actuel.</span><span class="sxs-lookup"><span data-stu-id="603c5-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="603c5-153">Des défaillances peuvent se produire sur Win16 si le nombre de processus dépasse un certain nombre, ou sur un système si la mémoire disponible est épuisée.</span><span class="sxs-lookup"><span data-stu-id="603c5-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="603c5-154">Initialise les variables globales partagées de tous les processus.</span><span class="sxs-lookup"><span data-stu-id="603c5-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="603c5-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="603c5-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="603c5-156">Il n’y avait pas assez de ressources système disponibles pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="603c5-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="603c5-157">Initialise le moteur de notification, crée sa fenêtre et son thread si l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS le demande.</span><span class="sxs-lookup"><span data-stu-id="603c5-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="603c5-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="603c5-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="603c5-159">Peut échouer si les ressources système sont épuisées.</span><span class="sxs-lookup"><span data-stu-id="603c5-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="603c5-160">Charge et initialise le fournisseur de profils.</span><span class="sxs-lookup"><span data-stu-id="603c5-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="603c5-161">Vérifie que **MAPIInitialize** peut accéder à la clé de Registre dans laquelle les données de profil sont stockées.</span><span class="sxs-lookup"><span data-stu-id="603c5-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="603c5-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="603c5-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="603c5-163">Le fournisseur de profils a rencontré une erreur.</span><span class="sxs-lookup"><span data-stu-id="603c5-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="603c5-164">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="603c5-164">MFCMAPI reference</span></span>

<span data-ttu-id="603c5-165">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="603c5-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="603c5-166">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="603c5-166">**File**</span></span>|<span data-ttu-id="603c5-167">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="603c5-167">**Function**</span></span>|<span data-ttu-id="603c5-168">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="603c5-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="603c5-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="603c5-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="603c5-170">MFCMAPI utilise la **méthode MAPIInitialize** pour initialiser MAPI sur un thread d’arrière-plan pour traiter certaines tables.</span><span class="sxs-lookup"><span data-stu-id="603c5-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="603c5-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603c5-171">See also</span></span>



[<span data-ttu-id="603c5-172">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="603c5-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

