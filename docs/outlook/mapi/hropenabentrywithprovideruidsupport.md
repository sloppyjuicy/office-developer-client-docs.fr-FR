---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347753"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="92e8c-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="92e8c-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="92e8c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92e8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92e8c-105">Effectue la même fonction que la fonction [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , sauf que la fonction **HrOpenABEntryWithProviderUIDSupport** ouvre l'entrée à l'aide de l'objet de prise en charge donné au lieu d'utiliser la session et le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="92e8c-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92e8c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="92e8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="92e8c-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="92e8c-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="92e8c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="92e8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="92e8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="92e8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="92e8c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="92e8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="92e8c-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="92e8c-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="92e8c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92e8c-112">Parameters</span></span>

 <span data-ttu-id="92e8c-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="92e8c-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="92e8c-114">dans Pointeur vers un paramètre _emsabpUID_ qui identifie le fournisseur de carnet d'adresses Exchange que cette fonction doit utiliser pour afficher les détails sur l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="92e8c-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="92e8c-115">Si l'identificateur d'entrée entrante n'est pas un identificateur d'entrée de fournisseur de carnet d'adresses Exchange, ce paramètre est ignoré et l'appel de fonction se comporte exactement comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="92e8c-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="92e8c-116">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction agit également exactement comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="92e8c-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="92e8c-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="92e8c-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="92e8c-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="92e8c-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="92e8c-119">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="92e8c-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="92e8c-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="92e8c-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="92e8c-121">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="92e8c-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="92e8c-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="92e8c-122">_lpInterface_</span></span>
  
> <span data-ttu-id="92e8c-123">dans Pointeur vers l'identificateur d'interface (IID) de l'interface à utiliser pour accéder à l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="92e8c-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="92e8c-124">Le passage de la valeur NULL renvoie l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="92e8c-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="92e8c-125">Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="92e8c-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="92e8c-126">Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs dont il est [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="92e8c-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="92e8c-127">Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="92e8c-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="92e8c-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="92e8c-128">_ulFlags_</span></span>
  
> <span data-ttu-id="92e8c-129">dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="92e8c-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="92e8c-130">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="92e8c-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="92e8c-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="92e8c-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="92e8c-132">Indique que les détails renvoient la valeur TRUE si les modifications sont réellement apportées à l'adresse; dans le cas contraire, la méthode Details renvoie FALSe.</span><span class="sxs-lookup"><span data-stu-id="92e8c-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="92e8c-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="92e8c-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="92e8c-134">Affiche la version modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="92e8c-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="92e8c-135">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="92e8c-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="92e8c-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="92e8c-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="92e8c-137">Affiche la version non modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="92e8c-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="92e8c-138">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="92e8c-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="92e8c-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92e8c-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="92e8c-140">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="92e8c-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="92e8c-141">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="92e8c-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="92e8c-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="92e8c-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="92e8c-143">remarquer Pointeur vers le type de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="92e8c-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="92e8c-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="92e8c-144">_lppUnk_</span></span>
  
> <span data-ttu-id="92e8c-145">remarquer Pointeur vers un pointeur de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="92e8c-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

