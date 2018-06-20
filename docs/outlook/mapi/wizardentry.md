---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2c307d18c5b62e5190aa10632a47a3f16b80e81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787472"
---
# <a name="wizardentry"></a><span data-ttu-id="e2e4d-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="e2e4d-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="e2e4d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2e4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2e4d-105">Définit une fonction de point d’entrée de service fournisseur qui appelle de l’Assistant profil pour récupérer suffisamment d’informations pour afficher les feuilles de propriétés de configuration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2e4d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e2e4d-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2e4d-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="e2e4d-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="e2e4d-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e2e4d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e2e4d-109">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e2e4d-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="e2e4d-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="e2e4d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e2e4d-111">Assistant profil MAPI</span><span class="sxs-lookup"><span data-stu-id="e2e4d-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="e2e4d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2e4d-112">Parameters</span></span>

 <span data-ttu-id="e2e4d-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="e2e4d-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="e2e4d-114">[in] Descripteur d’instances de la DLL du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="e2e4d-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="e2e4d-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="e2e4d-116">[out] Pointeur vers une chaîne qui contient le nom complet de la ressource de la boîte de dialogue qui doit être affichée par l’Assistant profil lors de la configuration.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="e2e4d-117">La taille maximale de la chaîne, y compris le terminateur NULL, est de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="e2e4d-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="e2e4d-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="e2e4d-119">[out] Pointeur vers une procédure de boîte de dialogue Windows standard qui sera appelée par l’Assistant profil pour notifier le fournisseur d’événements différents.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="e2e4d-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="e2e4d-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="e2e4d-121">[in] Pointeur vers une implémentation d’interface de propriété qui fournit l’accès aux propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="e2e4d-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="e2e4d-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="e2e4d-123">[in] Pointeur vers l’objet de prise en charge MAPI applicable à cette session.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2e4d-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e2e4d-124">Return value</span></span>

<span data-ttu-id="e2e4d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2e4d-125">S_OK</span></span> 
  
> <span data-ttu-id="e2e4d-126">Fonction **WIZARDENTRY** du fournisseur de services a été appelée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="e2e4d-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e2e4d-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e2e4d-128">Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2e4d-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2e4d-129">Remarks</span></span>

<span data-ttu-id="e2e4d-130">L’Assistant profil appelle la fonction **WIZARDENTRY** en fonction de lorsque celle-ci est prête afficher l’interface utilisateur de configuration du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="e2e4d-131">Lorsque l’Assistant profil est terminé de configurer tous les fournisseurs, il écrit les propriétés de configuration dans le profil en appelant [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="e2e4d-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e2e4d-132">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e2e4d-132">Notes to implementers</span></span>

<span data-ttu-id="e2e4d-133">Le nom de la fonction **WIZARDENTRY** en fonction de doit être placé dans l’entrée WIZARD_ENTRY_NAME MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="e2e4d-134">Le nom de la ressource est que de la ressource de la boîte de dialogue qui sera affiché dans le volet de l’Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="e2e4d-135">La ressource est passée arrière doit contenir toutes les pages dans une ressource de la boîte de dialogue unique.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="e2e4d-136">Lorsque l’Assistant profil reçoit cette ressource, il ignore le style de la boîte de dialogue, mais pas les styles du contrôle et crée tous les contrôles enfants de la page Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="e2e4d-137">Tous les contrôles sont masqués à l’origine.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-137">All controls are initially hidden.</span></span> <span data-ttu-id="e2e4d-138">Fournisseurs doivent s’assurer que les coordonnées de leurs contrôles sont zéro ou en partant de zéro, et qu’elles ne dépassent pas une largeur maximale de 200 unités de la boîte de dialogue et une hauteur maximale de 150 unités de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="e2e4d-139">Identificateurs de contrôle ci-dessous 400 sont réservés à l’Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="e2e4d-140">L’Assistant profil affiche le titre du fournisseur en gras au-dessus de l’interface du fournisseur utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="e2e4d-141">Le pointeur d’interface de propriété fourni dans le paramètre _lpMAPIProp_ doit être conservé par le fournisseur pour référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="e2e4d-142">Traite uniquement l’ensemble plus élémentaire des propriétés de l’Assistant profil et le fournisseur peut utiliser l’implémentation d’interface de propriété pour inclure les propriétés supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="e2e4d-143">Pendant la configuration, les fournisseurs doivent ajouter leurs propriétés de configuration à l’objet qui implémente l’interface de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="e2e4d-144">Une fois que tous les fournisseurs ont été configurés, l’Assistant profil ajoute ces propriétés dans le profil.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="e2e4d-145">Pour plus d’informations sur l’utilisation de cette fonction, voir [Configuration du Service de Message prise en charge](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="e2e4d-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

