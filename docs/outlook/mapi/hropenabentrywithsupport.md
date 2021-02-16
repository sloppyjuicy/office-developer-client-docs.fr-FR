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
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="f87b4-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f87b4-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="f87b4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f87b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f87b4-105">N’utilisez pas cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f87b4-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f87b4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f87b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="f87b4-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="f87b4-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="f87b4-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f87b4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f87b4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f87b4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f87b4-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f87b4-110">Called by:</span></span>  <br/> |<span data-ttu-id="f87b4-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f87b4-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f87b4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f87b4-112">Parameters</span></span>

 <span data-ttu-id="f87b4-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="f87b4-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="f87b4-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f87b4-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="f87b4-115">[in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="f87b4-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f87b4-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f87b4-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="f87b4-117">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f87b4-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="f87b4-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f87b4-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="f87b4-119">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="f87b4-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="f87b4-120">La transmission NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f87b4-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="f87b4-121">Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="f87b4-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="f87b4-122">Pour les listes de distribution, il s’agit [d’IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="f87b4-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="f87b4-123">Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="f87b4-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="f87b4-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f87b4-124">_ulFlags_</span></span>
  
> <span data-ttu-id="f87b4-125">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="f87b4-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="f87b4-126">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="f87b4-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="f87b4-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="f87b4-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="f87b4-128">Indique que details renvoie TRUE si des modifications sont réellement apportées à l’adresse ; Dans le cas contraire, Details renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="f87b4-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="f87b4-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="f87b4-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="f87b4-130">Affiche la version modale de la boîte de dialogue Adresse commune.</span><span class="sxs-lookup"><span data-stu-id="f87b4-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="f87b4-131">Cet indicateur s’exclue mutuellement avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="f87b4-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="f87b4-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="f87b4-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="f87b4-133">Affiche la version non modée de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="f87b4-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="f87b4-134">Cet indicateur s’exclue mutuellement avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="f87b4-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="f87b4-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f87b4-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f87b4-136">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f87b4-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f87b4-137">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="f87b4-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f87b4-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f87b4-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="f87b4-139">[out] Pointeur vers le type de l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="f87b4-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="f87b4-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="f87b4-140">_lppUnk_</span></span>
  
> <span data-ttu-id="f87b4-141">[out] Pointeur vers un pointeur de l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="f87b4-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

