---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578625"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="c13bf-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="c13bf-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="c13bf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c13bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c13bf-105">Ajoute un fournisseur de services pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="c13bf-105">Adds a service provider to the message service.</span></span> 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="c13bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c13bf-106">Parameters</span></span>

 <span data-ttu-id="c13bf-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="c13bf-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="c13bf-108">[in] Pointeur vers le nom du fournisseur à ajouter.</span><span class="sxs-lookup"><span data-stu-id="c13bf-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="c13bf-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="c13bf-109">_cValues_</span></span>
  
> <span data-ttu-id="c13bf-110">[in] Le nombre de valeurs de propriété indiqué par le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="c13bf-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="c13bf-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="c13bf-111">_lpProps_</span></span>
  
> <span data-ttu-id="c13bf-112">[in] Pointeur vers un tableau de valeurs de propriété qui décrit les propriétés du fournisseur à ajouter.</span><span class="sxs-lookup"><span data-stu-id="c13bf-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="c13bf-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c13bf-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="c13bf-114">[in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="c13bf-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="c13bf-115">Le paramètre _ulUIParam_ est utilisé si l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c13bf-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c13bf-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c13bf-116">_ulFlags_</span></span>
  
> <span data-ttu-id="c13bf-117">[in] Masque de bits d’indicateurs qui contrôle l’ajout du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c13bf-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="c13bf-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="c13bf-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="c13bf-119">MAPI_DIALOG : Affiche une boîte de dialogue pour demander des informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="c13bf-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="c13bf-120">MAPI_UNICODE : Les propriétés nom et la chaîne du fournisseur sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c13bf-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="c13bf-121">Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c13bf-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c13bf-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c13bf-122">_lpUID_</span></span>
  
> <span data-ttu-id="c13bf-123">[out] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à ajouter.</span><span class="sxs-lookup"><span data-stu-id="c13bf-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c13bf-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c13bf-124">Return value</span></span>

<span data-ttu-id="c13bf-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c13bf-125">S_OK</span></span> 
  
> <span data-ttu-id="c13bf-126">Le fournisseur a été ajouté au service de message.</span><span class="sxs-lookup"><span data-stu-id="c13bf-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="c13bf-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c13bf-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c13bf-128">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c13bf-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c13bf-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="c13bf-129">Remarks</span></span>

<span data-ttu-id="c13bf-130">La méthode **IProviderAdmin::CreateProvider** ajoute un fournisseur de services pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="c13bf-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="c13bf-131">Le paramètre _lpszProvider_ doit pointer sur le nom d’un fournisseur qui appartient au service de message.</span><span class="sxs-lookup"><span data-stu-id="c13bf-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="c13bf-132">**CreateProvider** ne vérifie pas si le nom correspond au nom d’un fournisseur de service ; Si le nom passé ne correspond pas à un nom de service, l’appel réussit, mais le résultat est imprévisible.</span><span class="sxs-lookup"><span data-stu-id="c13bf-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="c13bf-133">La plupart des services de messagerie ne permettent pas de fournisseurs être ajouté ou supprimé pendant que le profil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c13bf-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="c13bf-134">Après tout des informations disponibles sur le service fournisseur a été ajouté au profil à partir du fichier Mapisvc.inf, **CreateProvider** appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_ PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="c13bf-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="c13bf-135">Si MAPI_DIALOG est définie dans le paramètre de la méthode **CreateProvider** _ulFlags_ , les valeurs dans les paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c13bf-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="c13bf-136">Ces paramètres supplémentaires activer le fournisseur de services afficher sa feuille de propriétés afin que l’utilisateur puisse entrer des paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="c13bf-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c13bf-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c13bf-137">See also</span></span>

- [<span data-ttu-id="c13bf-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c13bf-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="c13bf-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c13bf-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="c13bf-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c13bf-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="c13bf-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c13bf-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

