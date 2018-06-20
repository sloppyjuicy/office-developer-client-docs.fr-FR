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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784126"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="e2e38-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="e2e38-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="e2e38-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2e38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2e38-105">Récupère les informations d’impression en cours.</span><span class="sxs-lookup"><span data-stu-id="e2e38-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="e2e38-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="e2e38-106">Parameters</span></span>

 <span data-ttu-id="e2e38-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2e38-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e2e38-108">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="e2e38-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="e2e38-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e2e38-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e2e38-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2e38-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e2e38-111">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2e38-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="e2e38-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e2e38-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e2e38-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="e2e38-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="e2e38-114">[out] Pointeur vers un pointeur vers une structure qui contient les informations d’impression.</span><span class="sxs-lookup"><span data-stu-id="e2e38-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2e38-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e2e38-115">Return value</span></span>

<span data-ttu-id="e2e38-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2e38-116">S_OK</span></span> 
  
> <span data-ttu-id="e2e38-117">Les informations d’impression a été récupérées correctement.</span><span class="sxs-lookup"><span data-stu-id="e2e38-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2e38-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2e38-118">Remarks</span></span>

<span data-ttu-id="e2e38-119">Objets formulaire appeler la méthode **IMAPIViewContext::GetPrintSetup** pour extraire des informations sur la configuration de l’imprimante avant d’imprimer le message en cours.</span><span class="sxs-lookup"><span data-stu-id="e2e38-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e2e38-120">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e2e38-120">Notes to implementers</span></span>

<span data-ttu-id="e2e38-121">Allouer les membres **hDevMode** et **hDevName** de la structure [FORMPRINTSETUP](formprintsetup.md) à l’aide de la fonction Win32 **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="e2e38-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2e38-122">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="e2e38-122">Notes to callers</span></span>

<span data-ttu-id="e2e38-123">Si vous envisagez l' **hDevMode** et **hDevName** les membres de la structure **FORMPRINTSETUP** désignés par le paramètre _lppFormPrintSetup_ chaînes Unicode, la valeur _ulFlags_ MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e2e38-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="e2e38-124">Dans le cas contraire, **GetPrintSetup** renverra ces chaînes au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e2e38-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="e2e38-125">Libérer les membres **hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** en appelant la fonction Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="e2e38-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="e2e38-126">Libérez de l’intégralité de la structure **FORMPRINTSETUP** en appelant [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e2e38-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2e38-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2e38-127">See also</span></span>



[<span data-ttu-id="e2e38-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="e2e38-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="e2e38-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2e38-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

