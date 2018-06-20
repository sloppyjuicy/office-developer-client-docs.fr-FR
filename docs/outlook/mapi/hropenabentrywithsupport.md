---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783575"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="50537-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="50537-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="50537-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50537-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50537-105">N’utilisez pas cette fonction.</span><span class="sxs-lookup"><span data-stu-id="50537-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50537-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="50537-106">Header file:</span></span>  <br/> |<span data-ttu-id="50537-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="50537-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="50537-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="50537-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="50537-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="50537-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="50537-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="50537-110">Called by:</span></span>  <br/> |<span data-ttu-id="50537-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="50537-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="50537-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50537-112">Parameters</span></span>

 <span data-ttu-id="50537-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="50537-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="50537-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="50537-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="50537-115">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="50537-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="50537-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="50537-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="50537-117">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="50537-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="50537-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="50537-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="50537-119">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée open.</span><span class="sxs-lookup"><span data-stu-id="50537-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="50537-120">Passage de NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="50537-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="50537-121">Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="50537-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="50537-122">Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md), et pour les conteneurs, il est [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="50537-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="50537-123">Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="50537-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="50537-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50537-124">_ulFlags_</span></span>
  
> <span data-ttu-id="50537-125">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="50537-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="50537-126">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="50537-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="50537-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="50537-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="50537-128">Indique que les détails renvoie la valeur TRUE si les modifications sont réellement apportées à l’adresse ; plus d’informations dans le cas contraire, renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="50537-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="50537-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="50537-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="50537-130">Affiche la version de la boîte de dialogue adresse modale.</span><span class="sxs-lookup"><span data-stu-id="50537-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="50537-131">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="50537-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="50537-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="50537-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="50537-133">Affiche la version de la boîte de dialogue adresse non modale.</span><span class="sxs-lookup"><span data-stu-id="50537-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="50537-134">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="50537-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="50537-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50537-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="50537-136">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="50537-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="50537-137">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="50537-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="50537-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="50537-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="50537-139">[out] Pointeur vers le type de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="50537-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="50537-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="50537-140">_lppUnk_</span></span>
  
> <span data-ttu-id="50537-141">[out] Pointeur vers un pointeur de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="50537-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

