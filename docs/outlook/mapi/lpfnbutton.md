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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b302de68f27e85c67430f82bd3e2c33009600e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591351"
---
# <a name="lpfnbutton"></a><span data-ttu-id="67471-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="67471-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="67471-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67471-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67471-105">Définit une fonction de rappel appels MAPI pour activer un contrôle bouton d’option dans une boîte de dialogue Carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="67471-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="67471-106">Ce bouton est généralement un bouton **Détails** .</span><span class="sxs-lookup"><span data-stu-id="67471-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67471-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="67471-107">Header file:</span></span>  <br/> |<span data-ttu-id="67471-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67471-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="67471-109">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="67471-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="67471-110">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="67471-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="67471-111">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="67471-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="67471-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="67471-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="67471-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67471-113">Parameters</span></span>

 <span data-ttu-id="67471-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="67471-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="67471-115">[in] Poignée de fenêtres parent pour toutes les boîtes de dialogue ou de windows qu'affiche cette fonction.</span><span class="sxs-lookup"><span data-stu-id="67471-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="67471-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="67471-116">_lpvContext_</span></span>
  
> <span data-ttu-id="67471-117">[in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="67471-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="67471-118">Cette valeur peut représenter une adresse de l’argument précision à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="67471-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="67471-119">En règle générale, pour le code C++, _lpvContext_ représente un pointeur vers un objet C++.</span><span class="sxs-lookup"><span data-stu-id="67471-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="67471-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="67471-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="67471-121">[in] Taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpSelection_ .</span><span class="sxs-lookup"><span data-stu-id="67471-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="67471-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="67471-122">_lpSelection_</span></span>
  
> <span data-ttu-id="67471-123">[in] Pointeur vers l’identificateur d’entrée définissant la sélection dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67471-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="67471-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="67471-124">_ulFlags_</span></span>
  
> <span data-ttu-id="67471-125">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="67471-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67471-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="67471-126">Return value</span></span>

<span data-ttu-id="67471-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="67471-127">S_OK</span></span> 
  
> <span data-ttu-id="67471-128">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="67471-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67471-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="67471-129">Remarks</span></span>

<span data-ttu-id="67471-130">Applications clientes appellent une fonction de rappel selon le prototype **LPFNBUTTON** permet de définir un bouton dans une boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="67471-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="67471-131">Le client transmet un pointeur vers la fonction de rappel dans les appels à la méthode [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="67471-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="67471-132">Fournisseurs de services appellent une fonction de raccordement selon le prototype **LPFNBUTTON** permet de définir un bouton dans une boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="67471-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="67471-133">Le fournisseur passe un pointeur vers cette fonction raccordement dans les appels à la méthode [IMAPISupport::Details](imapisupport-details.md) .</span><span class="sxs-lookup"><span data-stu-id="67471-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="67471-134">Dans les deux cas, lorsque la boîte de dialogue s’affiche et l’utilisateur clique sur le bouton défini, appels MAPI **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="67471-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67471-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67471-135">See also</span></span>



[<span data-ttu-id="67471-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="67471-136">BuildDisplayTable</span></span>](builddisplaytable.md)

