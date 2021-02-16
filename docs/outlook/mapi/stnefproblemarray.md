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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434262"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="232f7-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="232f7-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="232f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="232f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="232f7-105">Contient un tableau de structures **STnefProblem** décrivant un ou plusieurs problèmes de traitement qui se sont produits lors du codage ou du décodage d’un flux TNEF (Transport Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="232f7-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="232f7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="232f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="232f7-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="232f7-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="232f7-108">Members</span><span class="sxs-lookup"><span data-stu-id="232f7-108">Members</span></span>

 <span data-ttu-id="232f7-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="232f7-109">**cProblem**</span></span>
  
> <span data-ttu-id="232f7-110">Nombre d’éléments dans le tableau spécifié dans le **membre aProblem.**</span><span class="sxs-lookup"><span data-stu-id="232f7-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="232f7-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="232f7-111">**aProblem**</span></span>
  
> <span data-ttu-id="232f7-112">Tableau de structures [STnefProblem.](stnefproblem.md)</span><span class="sxs-lookup"><span data-stu-id="232f7-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="232f7-113">Chaque structure contient des informations sur un problème de traitement de propriété ou d’attribut.</span><span class="sxs-lookup"><span data-stu-id="232f7-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="232f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="232f7-114">Remarks</span></span>

<span data-ttu-id="232f7-115">Si un problème se produit lors du traitement des attributs ou des propriétés, un paramètre de sortie dans la méthode [ITnef::ExtractProps](itnef-extractprops.md) et dans la méthode [ITnef::Finish](itnef-finish.md) reçoivent chacun un pointeur vers une structure **STnefProblemArray** et **ExtractProps** et **Finish** retournent chacun la valeur MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="232f7-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="232f7-116">Cette valeur d’erreur indique qu’un problème s’est produit lors du traitement et qu’une structure **STnefProblemArray** a été générée.</span><span class="sxs-lookup"><span data-stu-id="232f7-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="232f7-117">Si une structure **STnefProblem** n’est pas générée pendant le traitement d’un attribut ou d’une propriété, l’application cliente peut continuer en présumant que le traitement de cet attribut ou propriété a réussi.</span><span class="sxs-lookup"><span data-stu-id="232f7-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="232f7-118">La seule exception se produit lorsque le problème survient lors du décodage d’un bloc d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="232f7-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="232f7-119">Si l’erreur s’est produite pendant ce décodage, MAPI_E_UNABLE_TO_COMPLETE peut être renvoyé en tant que [code SCODE](scode.md) dans la structure.</span><span class="sxs-lookup"><span data-stu-id="232f7-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="232f7-120">Dans ce cas, le décodage du composant correspondant au bloc est arrêté et le décodage se poursuit dans un autre composant.</span><span class="sxs-lookup"><span data-stu-id="232f7-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="232f7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="232f7-121">See also</span></span>



[<span data-ttu-id="232f7-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="232f7-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="232f7-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="232f7-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="232f7-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="232f7-124">MAPI Structures</span></span>](mapi-structures.md)

