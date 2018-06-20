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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787281"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="c0b47-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="c0b47-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="c0b47-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0b47-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0b47-105">Contient un tableau de structures **STnefProblem** décrivant une ou plusieurs des problèmes qui se sont produites pendant le codage de traitement ou de décodage d’un flux de Transport Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="c0b47-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0b47-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c0b47-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0b47-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="c0b47-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="c0b47-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c0b47-108">Members</span></span>

 <span data-ttu-id="c0b47-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="c0b47-109">**cProblem**</span></span>
  
> <span data-ttu-id="c0b47-110">Nombre d’éléments dans le tableau spécifié dans le membre **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="c0b47-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="c0b47-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="c0b47-111">**aProblem**</span></span>
  
> <span data-ttu-id="c0b47-112">Tableau de structures [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b47-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="c0b47-113">Chaque structure contient des informations sur une propriété ou d’un problème de traitement des attributs.</span><span class="sxs-lookup"><span data-stu-id="c0b47-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c0b47-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0b47-114">Remarks</span></span>

<span data-ttu-id="c0b47-115">Si un problème survient au cours d’attribut ou de traitement de la propriété, un paramètre de sortie dans la méthode [ITnef::ExtractProps](itnef-extractprops.md) et la méthode de [ITnef::Finish](itnef-finish.md) recevoir un pointeur vers une structure **STnefProblemArray** et le **ExtractProps **et **Terminer** chaque renvoient la valeur MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="c0b47-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="c0b47-116">Cette valeur d’erreur indique qu’un problème s’est produit lors du traitement et une structure **STnefProblemArray** a été générée.</span><span class="sxs-lookup"><span data-stu-id="c0b47-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="c0b47-117">Si une structure **STnefProblem** n’est pas générée lors du traitement d’un attribut ou une propriété, l’application cliente peut continuer en supposant que le traitement de cet attribut ou une propriété a réussi.</span><span class="sxs-lookup"><span data-stu-id="c0b47-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="c0b47-118">La seule exception se produit lorsque le problème est survenu lors de décodage d’un bloc d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="c0b47-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="c0b47-119">Si l’erreur s’est produite pendant cette décodage, MAPI_E_UNABLE_TO_COMPLETE peut être retourné en tant que le [SCODE](scode.md) dans la structure.</span><span class="sxs-lookup"><span data-stu-id="c0b47-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="c0b47-120">Dans ce cas, le décodage du composant correspondant au bloc est arrêté et de décodage se poursuit dans un autre composant.</span><span class="sxs-lookup"><span data-stu-id="c0b47-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0b47-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0b47-121">See also</span></span>



[<span data-ttu-id="c0b47-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="c0b47-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="c0b47-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="c0b47-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="c0b47-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c0b47-124">MAPI Structures</span></span>](mapi-structures.md)

