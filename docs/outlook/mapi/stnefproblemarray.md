---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563505"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="5dcbe-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="5dcbe-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="5dcbe-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dcbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dcbe-105">Contient un tableau de structures **STnefProblem** décrivant une ou plusieurs des problèmes qui se sont produites pendant le codage de traitement ou de décodage d’un flux de Transport Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="5dcbe-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5dcbe-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5dcbe-106">Header file:</span></span>  <br/> |<span data-ttu-id="5dcbe-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="5dcbe-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="5dcbe-108">Members</span><span class="sxs-lookup"><span data-stu-id="5dcbe-108">Members</span></span>

 <span data-ttu-id="5dcbe-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="5dcbe-109">**cProblem**</span></span>
  
> <span data-ttu-id="5dcbe-110">Nombre d’éléments dans le tableau spécifié dans le membre **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="5dcbe-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="5dcbe-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="5dcbe-111">**aProblem**</span></span>
  
> <span data-ttu-id="5dcbe-112">Tableau de structures [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="5dcbe-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="5dcbe-113">Chaque structure contient des informations sur une propriété ou d’un problème de traitement des attributs.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5dcbe-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dcbe-114">Remarks</span></span>

<span data-ttu-id="5dcbe-115">Si un problème survient au cours d’attribut ou de traitement de la propriété, un paramètre de sortie dans la méthode [ITnef::ExtractProps](itnef-extractprops.md) et la méthode de [ITnef::Finish](itnef-finish.md) recevoir un pointeur vers une structure **STnefProblemArray** et le **ExtractProps **et **Terminer** chaque renvoient la valeur MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="5dcbe-116">Cette valeur d’erreur indique qu’un problème s’est produit lors du traitement et une structure **STnefProblemArray** a été générée.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="5dcbe-117">Si une structure **STnefProblem** n’est pas générée lors du traitement d’un attribut ou une propriété, l’application cliente peut continuer en supposant que le traitement de cet attribut ou une propriété a réussi.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="5dcbe-118">La seule exception se produit lorsque le problème est survenu lors de décodage d’un bloc d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="5dcbe-119">Si l’erreur s’est produite pendant cette décodage, MAPI_E_UNABLE_TO_COMPLETE peut être retourné en tant que le [SCODE](scode.md) dans la structure.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="5dcbe-120">Dans ce cas, le décodage du composant correspondant au bloc est arrêté et de décodage se poursuit dans un autre composant.</span><span class="sxs-lookup"><span data-stu-id="5dcbe-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5dcbe-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dcbe-121">See also</span></span>



[<span data-ttu-id="5dcbe-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="5dcbe-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="5dcbe-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="5dcbe-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="5dcbe-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="5dcbe-124">MAPI Structures</span></span>](mapi-structures.md)

