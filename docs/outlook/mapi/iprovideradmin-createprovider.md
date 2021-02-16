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
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430804"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="2a722-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="2a722-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="2a722-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a722-105">Ajoute un fournisseur de services au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="2a722-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="2a722-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a722-106">Parameters</span></span>

 <span data-ttu-id="2a722-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="2a722-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="2a722-108">[in] Pointeur vers le nom du fournisseur à ajouter.</span><span class="sxs-lookup"><span data-stu-id="2a722-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="2a722-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="2a722-109">_cValues_</span></span>
  
> <span data-ttu-id="2a722-110">[in] Nombre de valeurs de propriétés pointées par _le paramètre lpProps._</span><span class="sxs-lookup"><span data-stu-id="2a722-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="2a722-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="2a722-111">_lpProps_</span></span>
  
> <span data-ttu-id="2a722-112">[in] Pointeur vers un tableau de valeurs de propriété qui décrit les propriétés du fournisseur à ajouter.</span><span class="sxs-lookup"><span data-stu-id="2a722-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="2a722-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2a722-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="2a722-114">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2a722-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="2a722-115">Le _paramètre ulUIParam_ est utilisé si l’MAPI_DIALOG est définie dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="2a722-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2a722-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2a722-116">_ulFlags_</span></span>
  
> <span data-ttu-id="2a722-117">[in] Masque de bits d’indicateurs qui contrôle l’ajout du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2a722-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="2a722-118">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="2a722-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="2a722-119">MAPI_DIALOG : affiche une boîte de dialogue pour fournir des informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="2a722-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="2a722-120">MAPI_UNICODE : le nom du fournisseur et les propriétés de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="2a722-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="2a722-121">Si l’MAPI_UNICODE n’est pas définie, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="2a722-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="2a722-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="2a722-122">_lpUID_</span></span>
  
> <span data-ttu-id="2a722-123">[out] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à ajouter.</span><span class="sxs-lookup"><span data-stu-id="2a722-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2a722-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2a722-124">Return value</span></span>

<span data-ttu-id="2a722-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a722-125">S_OK</span></span> 
  
> <span data-ttu-id="2a722-126">Le fournisseur a été ajouté au service de messagerie avec succès.</span><span class="sxs-lookup"><span data-stu-id="2a722-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="2a722-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2a722-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="2a722-128">L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2a722-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2a722-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a722-129">Remarks</span></span>

<span data-ttu-id="2a722-130">La **méthode IProviderAdmin::CreateProvider** ajoute un fournisseur de services au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="2a722-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="2a722-131">Le  _paramètre lpszProvider_ doit pointer vers le nom d’un fournisseur qui appartient au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="2a722-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="2a722-132">**CreateProvider ne** vérifie pas si le nom correspond au nom d’un fournisseur dans le service ; Si le nom transmis ne correspond pas à un nom de service, l’appel réussit, mais les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="2a722-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="2a722-133">La plupart des services de messagerie n’autorisent pas l’ajout ou la suppression de fournisseurs pendant l’utilisation du profil.</span><span class="sxs-lookup"><span data-stu-id="2a722-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="2a722-134">Une fois que toutes les informations disponibles sur le fournisseur de services ont été ajoutées au profil à partir du fichier Mapisvc.inf, **CreateProvider** appelle la fonction de point d’entrée du service de messagerie avec le paramètre  _ulContext_ paramétré sur MSG_SERVICE_PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="2a722-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="2a722-135">Si MAPI_DIALOG est définie dans le paramètre _ulFlags_ de la méthode **CreateProvider,** les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2a722-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="2a722-136">Ces paramètres supplémentaires permettent au fournisseur de services d’afficher sa feuille de propriétés afin que l’utilisateur puisse entrer les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="2a722-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a722-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a722-137">See also</span></span>

- [<span data-ttu-id="2a722-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2a722-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="2a722-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="2a722-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="2a722-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2a722-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="2a722-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a722-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

