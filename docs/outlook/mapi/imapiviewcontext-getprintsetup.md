---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425126"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="97977-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="97977-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="97977-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97977-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97977-105">Récupère les informations d’impression actuelles.</span><span class="sxs-lookup"><span data-stu-id="97977-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="97977-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97977-106">Parameters</span></span>

 <span data-ttu-id="97977-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97977-107">_ulFlags_</span></span>
  
> <span data-ttu-id="97977-108">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="97977-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="97977-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="97977-109">The following flag can be set:</span></span>
    
<span data-ttu-id="97977-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97977-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="97977-111">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="97977-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="97977-112">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="97977-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="97977-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="97977-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="97977-114">[out] Pointeur vers un pointeur vers une structure qui contient les informations d’impression.</span><span class="sxs-lookup"><span data-stu-id="97977-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="97977-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="97977-115">Return value</span></span>

<span data-ttu-id="97977-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="97977-116">S_OK</span></span> 
  
> <span data-ttu-id="97977-117">Les informations d’impression ont été récupérées avec succès.</span><span class="sxs-lookup"><span data-stu-id="97977-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97977-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="97977-118">Remarks</span></span>

<span data-ttu-id="97977-119">Les objets form appellent la méthode **IMAPIViewContext::GetPrintSetup** pour récupérer des informations sur la configuration de l’imprimante avant d’essayer d’imprimer le message actuel.</span><span class="sxs-lookup"><span data-stu-id="97977-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="97977-120">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="97977-120">Notes to implementers</span></span>

<span data-ttu-id="97977-121">Allouez **les membres hDevMode** et **hDevName** de la structure [FORMPRINTSETUP](formprintsetup.md) à l’aide de la fonction Win32 **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="97977-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="97977-122">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="97977-122">Notes to callers</span></span>

<span data-ttu-id="97977-123">Si vous vous attendez à ce que les membres **hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** pointés par le paramètre  _lppFormPrintSetup_ soient des chaînes Unicode, définissez  _ulFlags_ sur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="97977-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="97977-124">Sinon, **GetPrintSetup** retournera ces chaînes au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="97977-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="97977-125">Libérez **les membres hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** en appelant la fonction Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="97977-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="97977-126">Libérez toute la structure **FORMPRINTSETUP** en appelant [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="97977-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97977-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97977-127">See also</span></span>



[<span data-ttu-id="97977-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="97977-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="97977-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97977-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

