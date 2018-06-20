---
title: Exécuter MAPIInitialize
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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784759"
---
# <a name="mapiinitialize"></a><span data-ttu-id="213bc-103">Exécuter MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="213bc-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="213bc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="213bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="213bc-105">Incrémente le décompte de références du sous-système MAPI et initialise les données globales de la DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="213bc-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="213bc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="213bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="213bc-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="213bc-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="213bc-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="213bc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="213bc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="213bc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="213bc-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="213bc-110">Called by:</span></span>  <br/> |<span data-ttu-id="213bc-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="213bc-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="213bc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="213bc-112">Parameters</span></span>

 <span data-ttu-id="213bc-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="213bc-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="213bc-114">[in] Pointeur vers une structure [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="213bc-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="213bc-115">Le paramètre _lpMapiInit_ peut être défini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="213bc-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="213bc-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="213bc-116">Return value</span></span>

<span data-ttu-id="213bc-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="213bc-117">S_OK</span></span> 
  
> <span data-ttu-id="213bc-118">Le sous-système MAPI a été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="213bc-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="213bc-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="213bc-119">Remarks</span></span>

<span data-ttu-id="213bc-120">Les incréments de fonction **exécuter MAPIInitialize** le MAPI décompte de références pour le sous-système MAPI et la décrémente de fonction [MAPIUninitialize](mapiuninitialize.md) l’interne décompte de références.</span><span class="sxs-lookup"><span data-stu-id="213bc-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="213bc-121">Par conséquent, le nombre d’appels à une fonction doit correspondre au nombre d’appels à l’autre.</span><span class="sxs-lookup"><span data-stu-id="213bc-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="213bc-122">**Exécuter MAPIInitialize** renvoie S_OK si MAPI n’a pas déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="213bc-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="213bc-123">Un client ou fournisseur de services doit appeler **exécuter MAPIInitialize** avant d’effectuer n’importe quel autre appel MAPI.</span><span class="sxs-lookup"><span data-stu-id="213bc-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="213bc-124">Cela entraîne client ou le service fournisseur appelle renvoyer la valeur MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="213bc-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="213bc-125">Lorsque vous appelez **exécuter MAPIInitialize** à partir d’une application multithread, définissez le paramètre _lpMapiInit_ vers une structure [MAPIINIT_0](mapiinit_0.md) qui est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="213bc-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="213bc-126">**MAPIINIT_0** MAPIINIT = {0 MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="213bc-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="213bc-127">et l’appel :</span><span class="sxs-lookup"><span data-stu-id="213bc-127">and call:</span></span> 
  
 <span data-ttu-id="213bc-128">**Exécuter MAPIInitialize** (&amp;MAPIINIT) ;</span><span class="sxs-lookup"><span data-stu-id="213bc-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="213bc-129">Lorsque cette structure est déclarée, MAPI crée un thread distinct pour gérer la fenêtre de notification, qui se poursuit jusqu'à ce que le décompte de références initialize descend à zéro.</span><span class="sxs-lookup"><span data-stu-id="213bc-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="213bc-130">Un service Windows doit définir le membre **ulflags** de la structure **MAPIINIT_0** désigné par _lpMapiInit_ à MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="213bc-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="213bc-131">Impossible d’appeler **exécuter MAPIInitialize** ou **MAPIUninitialize** au sein d’une fonction Win32 **DllMain** ou toute autre fonction qui crée ou met fin à des threads.</span><span class="sxs-lookup"><span data-stu-id="213bc-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="213bc-132">Pour plus d’informations, voir [Utilisation des objets Thread-Safe](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="213bc-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="213bc-133">**Exécuter MAPIInitialize** ne renvoie pas les informations d’erreur étendue.</span><span class="sxs-lookup"><span data-stu-id="213bc-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="213bc-134">Contrairement à la plupart des appels MAPI, la signification de ses valeurs de retour est définie strictement pour correspondre à l’étape particulière de l’initialisation a échoué :</span><span class="sxs-lookup"><span data-stu-id="213bc-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="213bc-135">Vérifie les paramètres et les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="213bc-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="213bc-136">MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="213bc-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="213bc-137">Appelant transmis indicateur ou paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="213bc-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="213bc-138">Initialise les clés de Registre requises par MAPI et confirme le type du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="213bc-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="213bc-139">Cette étape se produit uniquement si le processus de client s’exécute en tant que service sous Windows et définit l’indicateur de SERVICE MAPI_NT dans la structure **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="213bc-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="213bc-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="213bc-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="213bc-141">Le processus appelant est un service Windows et clés de Registre requises par MAPI n’a pas peuvent être initialisés.</span><span class="sxs-lookup"><span data-stu-id="213bc-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="213bc-142">Des informations supplémentaires peuvent être disponibles dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="213bc-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="213bc-143">Vérifier la compatibilité de MAPI avec OLE, puis initialiser OLE.</span><span class="sxs-lookup"><span data-stu-id="213bc-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="213bc-144">Vérifie la compatibilité entre les versions actuelles de OLE et MAPI.</span><span class="sxs-lookup"><span data-stu-id="213bc-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="213bc-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="213bc-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="213bc-146">La version de OLE installée sur la station de travail n’est pas compatible avec cette version de MAPI.</span><span class="sxs-lookup"><span data-stu-id="213bc-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="213bc-147">Initialise OLE.</span><span class="sxs-lookup"><span data-stu-id="213bc-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="213bc-148">Au cours de cette étape uniquement, cette fonction peut renvoyer un code d’erreur non répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="213bc-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="213bc-149">Toute erreur _non_ répertoriés ici doit être supposé provenant de la fonction OLE **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="213bc-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="213bc-150">Initialise les variables globales par processus</span><span class="sxs-lookup"><span data-stu-id="213bc-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="213bc-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="213bc-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="213bc-152">MAPI définit les cadre spécifique dans le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="213bc-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="213bc-153">Échecs peuvent se produire si le nombre de processus dépasse un certain nombre de Win16, ou sur n’importe quel système si la mémoire disponible est saturée.</span><span class="sxs-lookup"><span data-stu-id="213bc-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="213bc-154">Initialise partagées des variables globales de tous les processus.</span><span class="sxs-lookup"><span data-stu-id="213bc-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="213bc-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="213bc-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="213bc-156">Pas de suffisamment de ressources système était disponibles pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="213bc-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="213bc-157">Initialise le moteur de notification, crée une fenêtre et son thread si demandée par l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="213bc-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="213bc-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="213bc-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="213bc-159">Peut échouer si épuisement des ressources système.</span><span class="sxs-lookup"><span data-stu-id="213bc-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="213bc-160">Charge et initialise le fournisseur de profils.</span><span class="sxs-lookup"><span data-stu-id="213bc-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="213bc-161">Vérifie que **exécuter MAPIInitialize** peut accéder à la clé de Registre où sont stockées les données de profil.</span><span class="sxs-lookup"><span data-stu-id="213bc-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="213bc-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="213bc-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="213bc-163">Le fournisseur de profils a rencontré une erreur.</span><span class="sxs-lookup"><span data-stu-id="213bc-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="213bc-164">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="213bc-164">MFCMAPI reference</span></span>

<span data-ttu-id="213bc-165">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="213bc-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="213bc-166">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="213bc-166">**File**</span></span>|<span data-ttu-id="213bc-167">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="213bc-167">**Function**</span></span>|<span data-ttu-id="213bc-168">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="213bc-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="213bc-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="213bc-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="213bc-170">MFCMAPI utilise la méthode **exécuter MAPIInitialize** pour initialiser MAPI sur une thread d’arrière-plan pour effectuer un traitement du tableau.</span><span class="sxs-lookup"><span data-stu-id="213bc-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="213bc-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="213bc-171">See also</span></span>



[<span data-ttu-id="213bc-172">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="213bc-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

