---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586010"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="99822-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="99822-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="99822-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99822-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99822-105">Effectue la même fonction que la fonction [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , sauf que la fonction **HrOpenABEntryWithProviderUIDSupport** ouvre l’entrée à l’aide de l’objet de prise en charge donné au lieu d’utiliser la session et le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="99822-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99822-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="99822-106">Header file:</span></span>  <br/> |<span data-ttu-id="99822-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="99822-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="99822-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="99822-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="99822-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="99822-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="99822-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="99822-110">Called by:</span></span>  <br/> |<span data-ttu-id="99822-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="99822-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="99822-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99822-112">Parameters</span></span>

 <span data-ttu-id="99822-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="99822-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="99822-114">[in] Pointeur vers un paramètre _emsabpUID_ qui identifie le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="99822-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="99822-115">Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée Exchange adresse livre fournisseur, ce paramètre est ignoré et la fonction appel exactement joue [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="99822-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="99822-116">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction comporte également exactement comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="99822-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="99822-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="99822-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="99822-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="99822-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="99822-119">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="99822-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="99822-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="99822-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="99822-121">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="99822-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="99822-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="99822-122">_lpInterface_</span></span>
  
> <span data-ttu-id="99822-123">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée open.</span><span class="sxs-lookup"><span data-stu-id="99822-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="99822-124">Passage de NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="99822-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="99822-125">Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="99822-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="99822-126">Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md)et il s’agit de conteneurs [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="99822-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="99822-127">Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="99822-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="99822-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99822-128">_ulFlags_</span></span>
  
> <span data-ttu-id="99822-129">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="99822-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="99822-130">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="99822-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="99822-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="99822-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="99822-132">Indique que les détails renvoie la valeur TRUE si les modifications sont réellement apportées à l’adresse ; plus d’informations dans le cas contraire, renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="99822-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="99822-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="99822-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="99822-134">Affiche la version de la boîte de dialogue adresse modale.</span><span class="sxs-lookup"><span data-stu-id="99822-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="99822-135">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="99822-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="99822-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="99822-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="99822-137">Affiche la version de la boîte de dialogue adresse non modale.</span><span class="sxs-lookup"><span data-stu-id="99822-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="99822-138">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="99822-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="99822-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="99822-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="99822-140">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="99822-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="99822-141">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="99822-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="99822-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="99822-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="99822-143">[out] Pointeur vers le type de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="99822-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="99822-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="99822-144">_lppUnk_</span></span>
  
> <span data-ttu-id="99822-145">[out] Pointeur vers un pointeur de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="99822-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

