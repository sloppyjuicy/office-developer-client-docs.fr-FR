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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430678"
---
# <a name="wizardentry"></a><span data-ttu-id="fcaba-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="fcaba-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="fcaba-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcaba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcaba-105">Définit une fonction de point d’entrée de fournisseur de services que l’Assistant Profil appelle pour récupérer suffisamment d’informations pour afficher les feuilles de propriétés de configuration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fcaba-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcaba-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fcaba-106">Header file:</span></span>  <br/> |<span data-ttu-id="fcaba-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="fcaba-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="fcaba-108">Fonction définie implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fcaba-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="fcaba-109">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fcaba-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="fcaba-110">Fonction définie appelée par :</span><span class="sxs-lookup"><span data-stu-id="fcaba-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="fcaba-111">Assistant Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="fcaba-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="fcaba-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcaba-112">Parameters</span></span>

 <span data-ttu-id="fcaba-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="fcaba-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="fcaba-114">[in] Handle d’instance de la DLL du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="fcaba-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="fcaba-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="fcaba-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="fcaba-116">[out] Pointeur vers une chaîne qui contient le nom complet de la ressource de boîte de dialogue qui doit être affichée par l’Assistant Profil pendant la configuration.</span><span class="sxs-lookup"><span data-stu-id="fcaba-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="fcaba-117">La taille maximale de la chaîne, y compris le terminateur NULL, est de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="fcaba-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="fcaba-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="fcaba-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="fcaba-119">[out] Pointeur vers une procédure de boîte de dialogue Windows standard qui sera appelée par l’Assistant Profil pour notifier le fournisseur de différents événements.</span><span class="sxs-lookup"><span data-stu-id="fcaba-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="fcaba-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="fcaba-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="fcaba-121">[in] Pointeur vers une implémentation d’interface de propriétés qui donne accès aux propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="fcaba-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="fcaba-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="fcaba-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="fcaba-123">[in] Pointeur vers l’objet de support MAPI applicable à cette session.</span><span class="sxs-lookup"><span data-stu-id="fcaba-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcaba-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fcaba-124">Return value</span></span>

<span data-ttu-id="fcaba-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcaba-125">S_OK</span></span> 
  
> <span data-ttu-id="fcaba-126">La fonction **WIZARDENTRY** du fournisseur de services a été appelée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fcaba-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="fcaba-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="fcaba-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="fcaba-128">Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fcaba-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcaba-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="fcaba-129">Remarks</span></span>

<span data-ttu-id="fcaba-130">L’Assistant Profil appelle **la fonction BASÉE SUR WIZARDENTRY** lorsqu’il est prêt à afficher l’interface utilisateur de configuration du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="fcaba-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="fcaba-131">Lorsque l’Assistant Profil a terminé de configurer tous les fournisseurs, il écrit les propriétés de configuration dans le profil en appelant [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="fcaba-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fcaba-132">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="fcaba-132">Notes to implementers</span></span>

<span data-ttu-id="fcaba-133">Le nom de la **fonction WIZARDENTRY** doit être placé dans l’entrée WIZARD_ENTRY_NAME dans MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="fcaba-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="fcaba-134">Le nom de la ressource est celui de la ressource de boîte de dialogue qui sera rendue dans le volet de l’Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="fcaba-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="fcaba-135">La ressource qui est passée en arrière doit contenir toutes les pages dans une seule ressource de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fcaba-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="fcaba-136">Lorsque l’Assistant Profil reçoit cette ressource, il ignore le style de la boîte de dialogue, mais pas les styles de contrôle, et crée tous les contrôles en tant qu’enfants de la page Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="fcaba-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="fcaba-137">Tous les contrôles sont initialement masqués.</span><span class="sxs-lookup"><span data-stu-id="fcaba-137">All controls are initially hidden.</span></span> <span data-ttu-id="fcaba-138">Les fournisseurs doivent s’assurer que les coordonnées de leurs contrôles sont de base zéro ou zéro, et qu’ils ne dépassent pas une largeur maximale de 200 unités de boîte de dialogue et une hauteur maximale de 150 unités de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fcaba-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="fcaba-139">Les identificateurs de contrôle inférieurs à 400 sont réservés à l’Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="fcaba-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="fcaba-140">L’Assistant Profil affiche le titre du fournisseur en gras au-dessus de l’interface utilisateur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fcaba-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="fcaba-141">Le pointeur d’interface de propriétés fourni dans le paramètre  _lpMAPIProp_ doit être conservé par le fournisseur pour référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fcaba-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="fcaba-142">L’Assistant Profil traite uniquement de l’ensemble de propriétés le plus élémentaire, et le fournisseur peut utiliser l’implémentation de l’interface de propriétés pour inclure des propriétés supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fcaba-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="fcaba-143">Pendant la configuration, les fournisseurs doivent ajouter leurs propriétés de configuration à l’objet qui implémente l’interface de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fcaba-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="fcaba-144">Une fois tous les fournisseurs configurés, l’Assistant Profil ajoute ces propriétés au profil.</span><span class="sxs-lookup"><span data-stu-id="fcaba-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="fcaba-145">Pour plus d’informations sur l’utilisation de cette fonction, voir Prise en charge [de la configuration du service de message.](supporting-message-service-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="fcaba-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

