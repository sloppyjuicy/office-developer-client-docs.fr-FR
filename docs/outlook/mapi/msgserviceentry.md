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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427877"
---
# <a name="msgserviceentry"></a><span data-ttu-id="98899-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="98899-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="98899-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98899-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98899-105">Définit un prototype pour une fonction de point d'entrée de service de message permettant de prendre en charge la configuration du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="98899-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98899-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="98899-106">Header file:</span></span>  <br/> |<span data-ttu-id="98899-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="98899-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="98899-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="98899-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="98899-109">Services de messagerie</span><span class="sxs-lookup"><span data-stu-id="98899-109">Message services</span></span>  <br/> |
|<span data-ttu-id="98899-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="98899-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="98899-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="98899-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="98899-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98899-112">Parameters</span></span>

 <span data-ttu-id="98899-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="98899-113">_hInstance_</span></span>
  
> <span data-ttu-id="98899-114">dans Handle de l'instance du service providerDLL.</span><span class="sxs-lookup"><span data-stu-id="98899-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="98899-115">Le descripteur est généralement utilisé pour récupérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="98899-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="98899-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="98899-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="98899-117">dans Pointeur vers un objet de l'allocation de mémoire qui expose \*\*\*\* l'interface OLE imalloc.</span><span class="sxs-lookup"><span data-stu-id="98899-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="98899-118">Le service de messagerie peut avoir besoin d'utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="98899-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="98899-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="98899-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="98899-120">dans Pointeur vers une implémentation d'interface [IUnknown IMAPISupport:](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="98899-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="98899-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="98899-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="98899-122">dans Valeur propre à l'implémentation utilisée pour passer des informations d'interface utilisateur à une fonction ou à zéro.</span><span class="sxs-lookup"><span data-stu-id="98899-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="98899-123">Le paramètre _ulUIParam_ est le descripteur de fenêtre parent de la boîte de dialogue de configuration et est de type HWND (Cast à a ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="98899-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="98899-124">La valeur zéro indique qu'il n'y a aucune fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="98899-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="98899-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98899-125">_ulFlags_</span></span>
  
> <span data-ttu-id="98899-126">dans Masque de réindicateur des indicateurs indiquant les options de la fonction d'entrée de service.</span><span class="sxs-lookup"><span data-stu-id="98899-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="98899-127">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="98899-127">The following flags can be set:</span></span>
    
<span data-ttu-id="98899-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98899-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="98899-129">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="98899-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="98899-130">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="98899-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="98899-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="98899-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="98899-132">L'interface utilisateur de configuration du service doit afficher la configuration actuelle, mais pas autoriser l'utilisateur à la modifier.</span><span class="sxs-lookup"><span data-stu-id="98899-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="98899-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="98899-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="98899-134">Permet l'affichage d'une boîte de dialogue de configuration si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="98899-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="98899-135">Lorsque l'indicateur SERVICE_UI_ALLOWED est défini, la boîte de dialogue ne doit être affichée que si le tableau de valeurs de la propriété _lpProps_ est vide ou ne contient pas une configuration valide.</span><span class="sxs-lookup"><span data-stu-id="98899-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="98899-136">Si SERVICE_UI_ALLOWED n'est pas défini, une boîte de dialogue peut toujours s'afficher si l'indicateur SERVICE_UI_ALWAYS est défini.</span><span class="sxs-lookup"><span data-stu-id="98899-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="98899-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="98899-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="98899-138">Demande que la boîte de dialogue de configuration pour le fournisseur actif s'affiche en haut des autres boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98899-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="98899-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="98899-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="98899-140">Le service de messagerie doit afficher une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="98899-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="98899-141">Si l'indicateur SERVICE_UI_ALWAYS n'est pas défini, une boîte de dialogue de configuration peut toujours s'afficher si l'indicateur SERVICE_UI_ALLOWED est défini et si des informations de configuration valides ne sont pas disponibles à partir du tableau de valeurs de la propriété _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="98899-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="98899-142">SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être défini pour permettre l'affichage de l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98899-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="98899-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="98899-143">_ulContext_</span></span>
  
> <span data-ttu-id="98899-144">dans Opération de configuration que MAPI effectue actuellement.</span><span class="sxs-lookup"><span data-stu-id="98899-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="98899-145">Le paramètre _ulContext_ contient l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="98899-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="98899-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="98899-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="98899-147">Les modifications apportées à la configuration du service doivent être effectuées dans le profil.</span><span class="sxs-lookup"><span data-stu-id="98899-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="98899-148">Si l'indicateur SERVICE_UI_ALWAYS est défini, le service doit afficher sa boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="98899-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="98899-149">La boîte de dialogue doit également être affichée si l'indicateur SERVICE_UI_ALLOWED est défini et si le paramètre _lpProps_ est vide ou ne contient pas de données de configuration valides.</span><span class="sxs-lookup"><span data-stu-id="98899-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="98899-150">Si _lpProps_ contient des données valides, aucune boîte de dialogue ne doit s'afficher et le service doit utiliser ces données pour procéder à la modification de la configuration.</span><span class="sxs-lookup"><span data-stu-id="98899-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="98899-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="98899-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="98899-152">Le service est ajouté à un profil.</span><span class="sxs-lookup"><span data-stu-id="98899-152">The service is being added to a profile.</span></span> <span data-ttu-id="98899-153">Si l'indicateur SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED est défini, le service doit afficher sa boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="98899-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="98899-154">Si aucun indicateur n'est défini, le service doit échouer.</span><span class="sxs-lookup"><span data-stu-id="98899-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="98899-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="98899-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="98899-156">Le service est en cours de suppression d'un profil.</span><span class="sxs-lookup"><span data-stu-id="98899-156">The service is being removed from a profile.</span></span> <span data-ttu-id="98899-157">Après réception de cet événement, le service doit retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="98899-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="98899-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="98899-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="98899-159">Le service a été installé sur la station de travail de l'utilisateur à partir d'un réseau, d'une disquette ou d'un autre support externe.</span><span class="sxs-lookup"><span data-stu-id="98899-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="98899-160">Après réception de cet événement, le service renvoie généralement S_OK.</span><span class="sxs-lookup"><span data-stu-id="98899-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="98899-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="98899-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="98899-162">Demande que le service crée une instance supplémentaire d'un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="98899-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="98899-163">Si le service prend en charge cette opération, il doit appeler [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="98899-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="98899-164">Si le service ne prend pas en charge cette opération, il peut renvoyer MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="98899-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="98899-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="98899-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="98899-166">Demande que le service supprime une instance de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="98899-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="98899-167">Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="98899-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="98899-168">Si le service ne prend pas en charge cette opération, il peut renvoyer MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="98899-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="98899-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="98899-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="98899-170">Le service est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="98899-170">The service is being removed.</span></span> <span data-ttu-id="98899-171">Après avoir reçu cet événement, le service peut effectuer toutes les tâches de nettoyage qui doivent être effectuées avant la fin du service, puis renvoyer avec une valeur de réussite.</span><span class="sxs-lookup"><span data-stu-id="98899-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="98899-172">Si l'utilisateur annule la suppression, le service doit renvoyer MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="98899-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="98899-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="98899-173">_cValues_</span></span>
  
> <span data-ttu-id="98899-174">dans Nombre de valeurs de propriété dans le tableau vers lequel pointe le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="98899-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="98899-175">La valeur du paramètre _cValues_ est égale à zéro si MAPI ne transmet aucune valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="98899-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="98899-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="98899-176">_lpProps_</span></span>
  
> <span data-ttu-id="98899-177">dans Pointeur vers un tableau facultatif de structures [SPropValue](spropvalue.md) indiquant des valeurs pour les propriétés prises en charge par le fournisseur que la fonction utilisera lors de la configuration du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="98899-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="98899-178">La fonction utilise ce paramètre uniquement si le paramètre _ulContext_ est défini sur MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="98899-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="98899-179">Ce paramètre est couramment utilisé pour transmettre le chemin d'accès à un fichier pour un service basé sur des fichiers, tel qu'un service de carnet d'adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="98899-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="98899-180">Si l'indicateur MSG_SERVICE_CONFIGURE n'est pas passé dans le paramètre _ulFlags_ , le paramètre _lpProps_ doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="98899-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="98899-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="98899-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="98899-182">dans Pointeur vers une interface [IProviderAdmin: IUnknown](iprovideradminiunknown.md) que la fonction peut utiliser pour localiser les sections de profil d'un fournisseur spécifique dans le service de messagerie actuel.</span><span class="sxs-lookup"><span data-stu-id="98899-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="98899-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="98899-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="98899-184">remarquer Pointeur vers une structure [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="98899-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="98899-185">La structure est allouée à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="98899-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="98899-186">Tous les membres sont facultatifs, bien que la plupart des structures contiennent une chaîne de message d'erreur valide dans le membre _lpszError_ .</span><span class="sxs-lookup"><span data-stu-id="98899-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="98899-187">Si les membres _lpszComponent_ ou _lpszError_ de la structure sont présents, leur mémoire doit éventuellement être libérée par un seul appel à [MAPIFreeBuffer](mapifreebuffer.md) sur la structure de base.</span><span class="sxs-lookup"><span data-stu-id="98899-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98899-188">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98899-188">Return value</span></span>

<span data-ttu-id="98899-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="98899-189">S_OK</span></span> 
  
> <span data-ttu-id="98899-190">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="98899-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="98899-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="98899-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="98899-192">Le fournisseur de services n'a pas été configuré.</span><span class="sxs-lookup"><span data-stu-id="98899-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="98899-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="98899-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="98899-194">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98899-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="98899-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="98899-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="98899-196">Le fournisseur ne prend pas en charge les modifications apportées à ses objets ou ne prend pas en charge la notification des modifications.</span><span class="sxs-lookup"><span data-stu-id="98899-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="98899-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="98899-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="98899-198">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="98899-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98899-199">Remarques</span><span class="sxs-lookup"><span data-stu-id="98899-199">Remarks</span></span>

<span data-ttu-id="98899-200">Une fonction définie à l'aide du prototype de fonction **MSGSERVICEENTRY** permet aux services de messagerie de se configurer eux-mêmes ou d'effectuer d'autres actions de service spécifiques.</span><span class="sxs-lookup"><span data-stu-id="98899-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="98899-201">La fonction fournit principalement une boîte de dialogue dans laquelle l'utilisateur peut modifier les paramètres propres au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="98899-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="98899-202">Il peut également prendre en charge la configuration par programme à l'aide du tableau de valeurs de propriété passé dans le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="98899-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="98899-203">La configuration par programme est facultative à moins que le service ne prenne en charge l'Assistant Profil, pour lequel il est requis.</span><span class="sxs-lookup"><span data-stu-id="98899-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="98899-204">MAPI appelle ce point d'entrée à partir de l'application du panneau de configuration ou en réponse à une application cliente qui appelle [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="98899-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="98899-205">MAPI ne place aucune restriction sur le nom de la fonction qu'un service de messagerie utilise pour le prototype **MSGSERVICEENTRY** mais préfère le nom **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="98899-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="98899-206">Il n'existe aucune restriction quant à l'ordinal de la fonction, et une seule DLL de fournisseur peut contenir plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="98899-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="98899-207">Toutefois, une seule des fonctions peut être nommée **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="98899-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="98899-208">Un service de messagerie peut utiliser la fonction [BuildDisplayTable](builddisplaytable.md) et la méthode [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) pour simplifier l'implémentation de la boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="98899-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="98899-209">Un utilisateur peut annuler une opération MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="98899-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="98899-210">Dans ce cas, la fonction **ServiceEntry** doit vérifier auprès de l'utilisateur que le service ne doit pas être supprimé et renvoyer MAPI_E_USER_CANCEL si le service reste installé.</span><span class="sxs-lookup"><span data-stu-id="98899-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="98899-211">Une fonction basée sur le prototype **MSGSERVICEENTRY** renvoie l'une des valeurs HRESULT indiquées.</span><span class="sxs-lookup"><span data-stu-id="98899-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="98899-212">MAPI transfère cette valeur lors de la réponse à l'appel d'un client à [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="98899-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="98899-213">Les services de messagerie qui exportent une fonction d'entrée de service doivent inclure les propriétés **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) et **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) dans la section service de messagerie de MAPISVC. INF.</span><span class="sxs-lookup"><span data-stu-id="98899-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

