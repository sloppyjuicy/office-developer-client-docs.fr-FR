---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417643"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="a2ddb-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="a2ddb-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="a2ddb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2ddb-105">N'utilisez pas cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2ddb-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a2ddb-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2ddb-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="a2ddb-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a2ddb-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a2ddb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2ddb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a2ddb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a2ddb-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a2ddb-110">Called by:</span></span>  <br/> |<span data-ttu-id="a2ddb-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a2ddb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a2ddb-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2ddb-112">Parameters</span></span>

 <span data-ttu-id="a2ddb-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="a2ddb-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="a2ddb-115">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a2ddb-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a2ddb-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="a2ddb-117">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="a2ddb-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="a2ddb-119">dans Pointeur vers l'identificateur d'interface (IID) de l'interface à utiliser pour accéder à l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="a2ddb-120">Le passage de la valeur NULL renvoie l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a2ddb-121">Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a2ddb-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a2ddb-122">Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il est [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a2ddb-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a2ddb-123">Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a2ddb-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a2ddb-125">dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="a2ddb-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="a2ddb-126">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="a2ddb-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="a2ddb-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a2ddb-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="a2ddb-128">Indique que les détails renvoient la valeur TRUE si les modifications sont réellement apportées à l'adresse; dans le cas contraire, la méthode Details renvoie FALSe.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="a2ddb-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="a2ddb-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="a2ddb-130">Affiche la version modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="a2ddb-131">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="a2ddb-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="a2ddb-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="a2ddb-133">Affiche la version non modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="a2ddb-134">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="a2ddb-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2ddb-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="a2ddb-136">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a2ddb-137">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a2ddb-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="a2ddb-139">remarquer Pointeur vers le type de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a2ddb-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a2ddb-140">_lppUnk_</span></span>
  
> <span data-ttu-id="a2ddb-141">remarquer Pointeur vers un pointeur de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="a2ddb-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

