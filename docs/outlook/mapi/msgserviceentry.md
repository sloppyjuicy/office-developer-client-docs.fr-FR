---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9af170f3445757eb96b9fe78c7cbea2c29ef4612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784919"
---
# <a name="msgserviceentry"></a><span data-ttu-id="a5edd-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="a5edd-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="a5edd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5edd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5edd-105">Définit un prototype pour une fonction point d’entrée message service prendre en charge la configuration du service de message.</span><span class="sxs-lookup"><span data-stu-id="a5edd-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5edd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a5edd-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5edd-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a5edd-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a5edd-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a5edd-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a5edd-109">Services de messagerie</span><span class="sxs-lookup"><span data-stu-id="a5edd-109">Message services</span></span>  <br/> |
|<span data-ttu-id="a5edd-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="a5edd-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a5edd-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5edd-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="a5edd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5edd-112">Parameters</span></span>

 <span data-ttu-id="a5edd-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="a5edd-113">_hInstance_</span></span>
  
> <span data-ttu-id="a5edd-114">[in] Handle de l’instance de le providerDLL service.</span><span class="sxs-lookup"><span data-stu-id="a5edd-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="a5edd-115">La poignée est généralement utilisée pour récupérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="a5edd-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="a5edd-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="a5edd-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="a5edd-117">[in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="a5edd-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="a5edd-118">Le service de message devrez peut-être utiliser cette méthode de répartition lorsque vous travaillez avec certaines interfaces comme **IStream**.</span><span class="sxs-lookup"><span data-stu-id="a5edd-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="a5edd-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="a5edd-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="a5edd-120">[in] Pointeur vers une [IMAPISupport : IUnknown](imapisupportiunknown.md) implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a5edd-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="a5edd-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a5edd-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="a5edd-122">[in] Une valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction ou à zéro.</span><span class="sxs-lookup"><span data-stu-id="a5edd-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="a5edd-123">Le paramètre _ulUIParam_ est le handle de fenêtre parent pour la boîte de dialogue de configuration et de type HWND (cast à un ULONG_PTR entière).</span><span class="sxs-lookup"><span data-stu-id="a5edd-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="a5edd-124">La valeur zéro indique qu’il n’existe aucune fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="a5edd-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="a5edd-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5edd-125">_ulFlags_</span></span>
  
> <span data-ttu-id="a5edd-126">[in] Masque de bits d’indicateurs indiquant les options pour la fonction de l’entrée de service.</span><span class="sxs-lookup"><span data-stu-id="a5edd-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="a5edd-127">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="a5edd-127">The following flags can be set:</span></span>
    
<span data-ttu-id="a5edd-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5edd-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a5edd-129">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5edd-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a5edd-130">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="a5edd-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="a5edd-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="a5edd-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="a5edd-132">Interface utilisateur de configuration du service doit afficher la configuration actuelle, mais pas autoriser l’utilisateur à modifier.</span><span class="sxs-lookup"><span data-stu-id="a5edd-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="a5edd-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="a5edd-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="a5edd-134">Permet à une boîte de dialogue de configuration à afficher si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a5edd-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="a5edd-135">Lors de l’indicateur SERVICE_UI_ALLOWED est défini, la boîte de dialogue doit être affichée uniquement si le tableau de valeurs de propriété _lpProps_ est vide ou ne contient-elle pas une configuration valide.</span><span class="sxs-lookup"><span data-stu-id="a5edd-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="a5edd-136">Si SERVICE_UI_ALLOWED n’est pas défini, une boîte de dialogue peut toujours être affichée si l’indicateur SERVICE_UI_ALWAYS est défini.</span><span class="sxs-lookup"><span data-stu-id="a5edd-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="a5edd-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="a5edd-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="a5edd-138">Demande que la boîte de dialogue configuration pour le fournisseur active affiche par-dessus les autres boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a5edd-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="a5edd-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="a5edd-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="a5edd-140">Requiert le service de message pour afficher une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="a5edd-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="a5edd-141">Si l’indicateur SERVICE_UI_ALWAYS n’est pas définie, une boîte de dialogue configuration peut toujours être affichée si l’indicateur SERVICE_UI_ALLOWED est défini et que les informations de configuration valides ne sont pas disponibles dans le tableau de valeurs de propriété _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a5edd-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="a5edd-142">SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être définie pour autoriser une interface utilisateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="a5edd-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="a5edd-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="a5edd-143">_ulContext_</span></span>
  
> <span data-ttu-id="a5edd-144">[in] L’opération de configuration MAPI exécute actuellement.</span><span class="sxs-lookup"><span data-stu-id="a5edd-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="a5edd-145">Le paramètre _ulContext_ contient une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5edd-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="a5edd-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="a5edd-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="a5edd-147">Modifications apportées à la configuration du service doivent être effectuées dans le profil.</span><span class="sxs-lookup"><span data-stu-id="a5edd-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="a5edd-148">Si l’indicateur SERVICE_UI_ALWAYS est défini, le service doit afficher la boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="a5edd-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="a5edd-149">La boîte de dialogue doit également être affichée si l’indicateur SERVICE_UI_ALLOWED est défini et que le paramètre _lpProps_ est vide ou ne contient-elle pas de données de configuration valides.</span><span class="sxs-lookup"><span data-stu-id="a5edd-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="a5edd-150">Si _lpProps_ contient des données valides, aucune boîte de dialogue ne doit s’afficher et le service doit utiliser ces données pour effectuer la modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="a5edd-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="a5edd-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="a5edd-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="a5edd-152">Le service est ajouté à un profil.</span><span class="sxs-lookup"><span data-stu-id="a5edd-152">The service is being added to a profile.</span></span> <span data-ttu-id="a5edd-153">Si l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS est défini, le service doit afficher la boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="a5edd-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="a5edd-154">Si aucun indicateur n’est défini, le service doit échouer.</span><span class="sxs-lookup"><span data-stu-id="a5edd-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="a5edd-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a5edd-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="a5edd-156">Le service est en cours de suppression d’un profil.</span><span class="sxs-lookup"><span data-stu-id="a5edd-156">The service is being removed from a profile.</span></span> <span data-ttu-id="a5edd-157">Après avoir reçu cet événement, le service doit renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="a5edd-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="a5edd-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="a5edd-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="a5edd-159">Le service a été installé sur le poste de travail à partir d’un réseau, disquette ou autre support externe.</span><span class="sxs-lookup"><span data-stu-id="a5edd-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="a5edd-160">Après avoir reçu cet événement, le service renvoie généralement S_OK.</span><span class="sxs-lookup"><span data-stu-id="a5edd-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="a5edd-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="a5edd-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="a5edd-162">Demande que le service crée une instance supplémentaire d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a5edd-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="a5edd-163">Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a5edd-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="a5edd-164">Si le service ne prend pas en charge cette opération, il peut retourner MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a5edd-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="a5edd-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="a5edd-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="a5edd-166">Demande que le service de supprime une instance de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a5edd-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="a5edd-167">Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a5edd-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="a5edd-168">Si le service ne prend pas en charge cette opération, il peut retourner MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a5edd-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="a5edd-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="a5edd-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="a5edd-170">Le service est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="a5edd-170">The service is being removed.</span></span> <span data-ttu-id="a5edd-171">Après avoir reçu cet événement, le service peut effectuer des tâches de nettoyage qui doivent être effectuées avant le service se termine et puis renvoie une valeur de réussite.</span><span class="sxs-lookup"><span data-stu-id="a5edd-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="a5edd-172">Si l’utilisateur annule la suppression, le service doit retourner MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="a5edd-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="a5edd-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="a5edd-173">_cValues_</span></span>
  
> <span data-ttu-id="a5edd-174">[in] Nombre de valeurs de propriété dans le tableau indiqué par le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a5edd-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="a5edd-175">La valeur du paramètre _cValues_ est égale à zéro si MAPI ne transmet aucune valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="a5edd-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="a5edd-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="a5edd-176">_lpProps_</span></span>
  
> <span data-ttu-id="a5edd-177">[in] Pointeur vers un tableau facultatif de [SPropValue](spropvalue.md) structures indiquant les valeurs des propriétés de fournisseur pris en charge qui utilise la fonction de la configuration du service de message.</span><span class="sxs-lookup"><span data-stu-id="a5edd-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="a5edd-178">La fonction utilise uniquement ce paramètre si le paramètre _ulContext_ est défini sur MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="a5edd-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="a5edd-179">Ce paramètre est généralement utilisé pour transmettre le chemin d’accès à un fichier pour un service basé sur le fichier, comme un service de carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="a5edd-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="a5edd-180">Si l’indicateur MSG_SERVICE_CONFIGURE n’est pas transmis dans le paramètre _ulFlags_ , le paramètre _lpProps_ doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a5edd-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="a5edd-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="a5edd-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="a5edd-182">[in] Pointeur vers une interface [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que la fonction peut utiliser pour rechercher les sections de profil pour un fournisseur spécifique dans le service de message en cours.</span><span class="sxs-lookup"><span data-stu-id="a5edd-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="a5edd-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="a5edd-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="a5edd-184">[out] Pointeur vers une structure [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="a5edd-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="a5edd-185">La structure est allouée avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a5edd-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="a5edd-186">Tous les membres sont facultatifs, bien que la plupart des structures contient une chaîne de message d’erreur valide dans le membre _lpszError_ .</span><span class="sxs-lookup"><span data-stu-id="a5edd-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="a5edd-187">Si les membres _lpszComponent_ ou _lpszError_ de la structure sont présentes, leur mémoire doit finalement libérée par un simple appel à [MAPIFreeBuffer](mapifreebuffer.md) sur la structure de base.</span><span class="sxs-lookup"><span data-stu-id="a5edd-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a5edd-188">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a5edd-188">Return value</span></span>

<span data-ttu-id="a5edd-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5edd-189">S_OK</span></span> 
  
> <span data-ttu-id="a5edd-190">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a5edd-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a5edd-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="a5edd-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="a5edd-192">Le fournisseur de services n’a pas été configuré.</span><span class="sxs-lookup"><span data-stu-id="a5edd-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="a5edd-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a5edd-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a5edd-194">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a5edd-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="a5edd-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a5edd-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a5edd-196">Le fournisseur ne prend pas en charge les modifications apportées à ses objets ou ne prend pas en charge la notification des modifications.</span><span class="sxs-lookup"><span data-stu-id="a5edd-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="a5edd-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a5edd-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a5edd-198">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5edd-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5edd-199">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5edd-199">Remarks</span></span>

<span data-ttu-id="a5edd-200">Une fonction définie à l’aide du prototype de la fonction **MSGSERVICEENTRY** permet de services de messagerie pour configurer eux-mêmes ou pour effectuer d’autres actions spécifiques au service.</span><span class="sxs-lookup"><span data-stu-id="a5edd-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="a5edd-201">La fonction fournit principalement une boîte de dialogue dans laquelle l’utilisateur peut modifier les paramètres spécifiques au service de message.</span><span class="sxs-lookup"><span data-stu-id="a5edd-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="a5edd-202">Il peut également prendre en charge de configuration par programme en utilisant le tableau de valeurs de propriété passé dans le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a5edd-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="a5edd-203">Configuration par programme est facultative, sauf si le service prend en charge l’Assistant profil, pour laquelle il est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a5edd-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="a5edd-204">Les appels MAPI ce point d’entrée de l’application du Panneau de configuration ou en réponse à une application cliente appelant [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a5edd-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="a5edd-205">MAPI ne place aucune restriction sur le nom de la fonction qu’un service de message utilise pour le prototype **MSGSERVICEENTRY** mais préfère le nom **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="a5edd-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="a5edd-206">Il n’existe aucune restriction sur le nombre ordinal de la fonction et un fournisseur unique DLL peut contenir plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="a5edd-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="a5edd-207">Toutefois, une seule des fonctions peut être nommée **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="a5edd-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="a5edd-208">Un service de message peut utiliser la fonction [BuildDisplayTable](builddisplaytable.md) et la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) pour simplifier l’implémentation de boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="a5edd-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="a5edd-209">Il est possible pour un utilisateur d’annuler une opération MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="a5edd-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="a5edd-210">Dans ce cas, la fonction **ServiceEntry** doit vérifier avec l’utilisateur pour vérifier que le service ne doivent pas être supprimés et renvoyer MAPI_E_USER_CANCEL si le service est toujours installé.</span><span class="sxs-lookup"><span data-stu-id="a5edd-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="a5edd-211">Une fonction basée sur le prototype **MSGSERVICEENTRY** renvoie une des valeurs HRESULT répertoriées.</span><span class="sxs-lookup"><span data-stu-id="a5edd-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="a5edd-212">MAPI transfère cette valeur lors de la réponse à l’appel d’un client à [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a5edd-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="a5edd-213">Services de messagerie à exporter une fonction d’entrée de service doivent inclure le **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) et les propriétés de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) dans la section service de message de MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="a5edd-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

