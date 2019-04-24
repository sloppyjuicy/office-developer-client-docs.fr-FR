---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357441"
---
# <a name="lpfnbutton"></a><span data-ttu-id="3a663-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="3a663-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="3a663-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a663-105">Définit une fonction de rappel que MAPI appelle pour activer un contrôle bouton facultatif dans une boîte de dialogue Carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="3a663-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="3a663-106">Ce bouton est généralement un bouton **Détails** .</span><span class="sxs-lookup"><span data-stu-id="3a663-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a663-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3a663-107">Header file:</span></span>  <br/> |<span data-ttu-id="3a663-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3a663-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3a663-109">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="3a663-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3a663-110">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="3a663-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="3a663-111">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="3a663-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3a663-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="3a663-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3a663-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a663-113">Parameters</span></span>

 <span data-ttu-id="3a663-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3a663-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="3a663-115">dans Handle des fenêtres parentes pour les boîtes de dialogue ou les fenêtres que cette fonction affiche.</span><span class="sxs-lookup"><span data-stu-id="3a663-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="3a663-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="3a663-116">_lpvContext_</span></span>
  
> <span data-ttu-id="3a663-117">dans Pointeur vers une valeur arbitraire passée à la fonction de rappel lorsque MAPI l'appelle.</span><span class="sxs-lookup"><span data-stu-id="3a663-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="3a663-118">Cette valeur peut représenter une adresse de l'importance de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="3a663-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="3a663-119">En règle générale, pour le code C++, _lpvContext_ représente un pointeur vers un objet c++.</span><span class="sxs-lookup"><span data-stu-id="3a663-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="3a663-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3a663-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="3a663-121">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpSelection_ .</span><span class="sxs-lookup"><span data-stu-id="3a663-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="3a663-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="3a663-122">_lpSelection_</span></span>
  
> <span data-ttu-id="3a663-123">dans Pointeur vers l'identificateur d'entrée qui définit la sélection dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3a663-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="3a663-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3a663-124">_ulFlags_</span></span>
  
> <span data-ttu-id="3a663-125">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="3a663-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3a663-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3a663-126">Return value</span></span>

<span data-ttu-id="3a663-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a663-127">S_OK</span></span> 
  
> <span data-ttu-id="3a663-128">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="3a663-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a663-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a663-129">Remarks</span></span>

<span data-ttu-id="3a663-130">Les applications clientes appellent une fonction de rappel basée sur le prototype **LPFNBUTTON** pour définir un bouton dans une boîte de dialogue détails.</span><span class="sxs-lookup"><span data-stu-id="3a663-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="3a663-131">Le client transmet un pointeur vers la fonction de rappel dans les appels à la méthode [IAddrBook::D etails](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="3a663-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="3a663-132">Les fournisseurs de services appellent une fonction de raccordement basée sur le prototype **LPFNBUTTON** pour définir un bouton dans une boîte de dialogue détails.</span><span class="sxs-lookup"><span data-stu-id="3a663-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="3a663-133">Le fournisseur transmet un pointeur vers cette fonction de raccordement dans les appels à la méthode [IMAPISupport::D etails](imapisupport-details.md) .</span><span class="sxs-lookup"><span data-stu-id="3a663-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="3a663-134">Dans les deux cas, lorsque la boîte de dialogue est affichée et que l'utilisateur choisit le bouton défini, MAPI appelle **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="3a663-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a663-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a663-135">See also</span></span>



[<span data-ttu-id="3a663-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="3a663-136">BuildDisplayTable</span></span>](builddisplaytable.md)

