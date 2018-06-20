---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787270"
---
# <a name="stnefproblem"></a><span data-ttu-id="2fb78-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="2fb78-103">STnefProblem</span></span>

  
  
<span data-ttu-id="2fb78-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fb78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fb78-105">Contient des informations sur un problème de traitement de l’attribut ou propriété qui s’est produite pendant le codage ou de décodage d’un flux de Transport Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="2fb78-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2fb78-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2fb78-106">Header file:</span></span>  <br/> |<span data-ttu-id="2fb78-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="2fb78-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="2fb78-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2fb78-108">Members</span></span>

 <span data-ttu-id="2fb78-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="2fb78-109">**ulComponent**</span></span>
  
> <span data-ttu-id="2fb78-110">Le type de traitement au cours de laquelle le problème est survenu.</span><span class="sxs-lookup"><span data-stu-id="2fb78-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="2fb78-111">Si le problème est survenu lors du traitement des messages, le membre **ulComponent** est défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2fb78-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="2fb78-112">Si le problème s’est produite pendant le traitement des pièces jointes, **ulComponent** est égale à la valeur **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe correspondante.</span><span class="sxs-lookup"><span data-stu-id="2fb78-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="2fb78-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="2fb78-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="2fb78-114">Attribut associé à la propriété indiquée par le membre **ulPropTag** ou lorsque le problème de traitement TNEF se produit quand une encapsulation de décodage bloquer, une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fb78-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="2fb78-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="2fb78-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="2fb78-116">Niveau de message</span><span class="sxs-lookup"><span data-stu-id="2fb78-116">Message level</span></span>
    
 <span data-ttu-id="2fb78-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="2fb78-117">_attAttachment_</span></span>
  
> <span data-ttu-id="2fb78-118">Au niveau de la pièce jointe</span><span class="sxs-lookup"><span data-stu-id="2fb78-118">Attachment level</span></span>
    
 <span data-ttu-id="2fb78-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="2fb78-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="2fb78-120">Balise de propriété de la propriété qui a provoqué le problème de traitement TNEF, sauf lorsque le problème se produit lors du décodage d’un bloc d’encapsulation, dans lequel cas **ulPropTag** est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2fb78-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="2fb78-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="2fb78-121">**scode**</span></span>
  
> <span data-ttu-id="2fb78-122">Valeur d’erreur indiquant le problème rencontré lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="2fb78-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2fb78-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="2fb78-123">Remarks</span></span>

<span data-ttu-id="2fb78-124">Si une structure **STnefProblem** n’est pas générée lors du traitement d’un attribut ou une propriété, l’application peut poursuivre en supposant que le traitement de cet attribut ou une propriété a réussi.</span><span class="sxs-lookup"><span data-stu-id="2fb78-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="2fb78-125">La seule exception se produit lorsque le problème est survenu lors de décodage d’un bloc d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="2fb78-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="2fb78-126">Dans ce cas, le décodage du composant correspondant au bloc est arrêté et de décodage se poursuit dans un autre composant.</span><span class="sxs-lookup"><span data-stu-id="2fb78-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fb78-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fb78-127">See also</span></span>



[<span data-ttu-id="2fb78-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="2fb78-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="2fb78-129">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="2fb78-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="2fb78-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2fb78-130">MAPI Structures</span></span>](mapi-structures.md)

