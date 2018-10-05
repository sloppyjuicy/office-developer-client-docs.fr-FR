---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386571"
---
# <a name="formprintsetup"></a><span data-ttu-id="07483-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="07483-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="07483-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07483-105">Décrit les informations de configuration de l’impression de l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="07483-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07483-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="07483-106">Header file:</span></span>  <br/> |<span data-ttu-id="07483-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="07483-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a><span data-ttu-id="07483-108">Members</span><span class="sxs-lookup"><span data-stu-id="07483-108">Members</span></span>

 <span data-ttu-id="07483-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="07483-109">**ulFlags**</span></span>
  
> <span data-ttu-id="07483-110">Masque de bits d’indicateurs qui contrôle le type des chaînes.</span><span class="sxs-lookup"><span data-stu-id="07483-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="07483-111">L’indicateur suivantes peut être utilisées :</span><span class="sxs-lookup"><span data-stu-id="07483-111">The following flag can be used:</span></span>
    
<span data-ttu-id="07483-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07483-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="07483-113">Les chaînes sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="07483-113">The strings are in Unicode format.</span></span> <span data-ttu-id="07483-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="07483-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="07483-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="07483-115">**hDevmode**</span></span>
  
> <span data-ttu-id="07483-116">Handle vers le mode de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="07483-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="07483-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="07483-117">**hDevnames**</span></span>
  
> <span data-ttu-id="07483-118">Gérer le chemin d’accès de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="07483-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="07483-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="07483-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="07483-120">Numéro de page de la première page à imprimer.</span><span class="sxs-lookup"><span data-stu-id="07483-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="07483-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="07483-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="07483-122">Indicateur qui indique s’il existe des pièces jointes à imprimer.</span><span class="sxs-lookup"><span data-stu-id="07483-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="07483-123">S’il existe des pièces jointes à imprimer, le membre **ulFPrintAttachments** est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="07483-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="07483-124">S’il n’y a pas de pièces jointes à imprimer, elle est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="07483-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="07483-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="07483-125">Remarks</span></span>

<span data-ttu-id="07483-126">La structure **FORMPRINTSETUP** est utilisée pour décrire les informations de configuration de l’impression d’un objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="07483-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="07483-127">Les implémentations de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) remplir la structure **FORMPRINTSETUP** et retourner dans le contenu du paramètre de sortie _lppFormPrintSetup_ de **GetPrintSetup**.</span><span class="sxs-lookup"><span data-stu-id="07483-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="07483-128">Si l’indicateur MAPI_UNICODE est passé dans le paramètre _ulFlags_ de **GetPrintSetup**, les chaînes référencées par les membres **hDevmode** et **hDevnames** doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="07483-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="07483-129">Dans le cas contraire, les chaînes doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="07483-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="07483-130">Visionneuses de formulaire l’implémentation **IMAPIViewContext** doivent affecter la structure **FORMPRINTSETUP** à l’aide de la fonction d’allocation MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), mais allouer les membres individuels, **hDevMode** et **hDevNames**, avec la fonction Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="07483-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="07483-131">La version de la mémoire est gérée de la même manière.</span><span class="sxs-lookup"><span data-stu-id="07483-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="07483-132">Les membres **hDevMode** et **hDevNames** doivent être libérés à l’aide de la fonction Windows [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) tandis que la structure **FORMPRINTSETUP** doit être libérée avec la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="07483-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07483-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07483-133">See also</span></span>



[<span data-ttu-id="07483-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="07483-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="07483-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="07483-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="07483-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="07483-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="07483-137">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="07483-137">MAPI Structures</span></span>](mapi-structures.md)

