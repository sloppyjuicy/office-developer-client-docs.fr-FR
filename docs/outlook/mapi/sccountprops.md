---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 97dad50fed4179526e46381c4d9ea9d12d568377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787092"
---
# <a name="sccountprops"></a><span data-ttu-id="1aee1-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="1aee1-103">ScCountProps</span></span>

  
  
<span data-ttu-id="1aee1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1aee1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1aee1-105">Détermine la taille, en octets, d’un tableau de valeurs de propriété et valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="1aee1-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1aee1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1aee1-106">Header file:</span></span>  <br/> |<span data-ttu-id="1aee1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1aee1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1aee1-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="1aee1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1aee1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1aee1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1aee1-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="1aee1-110">Called by:</span></span>  <br/> |<span data-ttu-id="1aee1-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1aee1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="1aee1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1aee1-112">Parameters</span></span>

 <span data-ttu-id="1aee1-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="1aee1-113">_cprop_</span></span>
  
> <span data-ttu-id="1aee1-114">[in] Nombre de propriétés dans le tableau indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="1aee1-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1aee1-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="1aee1-115">_rgprop_</span></span>
  
> <span data-ttu-id="1aee1-116">[in] Pointeur vers une plage dans un tableau de structures [SPropValue](spropvalue.md) qui définit les propriétés dont la taille est déterminée.</span><span class="sxs-lookup"><span data-stu-id="1aee1-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="1aee1-117">Cette plage ne démarre pas nécessairement au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="1aee1-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="1aee1-118">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="1aee1-118">_pcb_</span></span>
  
> <span data-ttu-id="1aee1-119">[out] Pointeur facultatif à la taille, en octets, du tableau de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1aee1-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1aee1-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1aee1-120">Return value</span></span>

<span data-ttu-id="1aee1-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="1aee1-121">S_OK</span></span> 
  
> <span data-ttu-id="1aee1-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1aee1-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1aee1-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1aee1-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1aee1-124">Au moins une propriété dans le tableau de valeurs de propriété est un identificateur de PROP_ID_NULL ou PROP_ID_INVALID, ou le tableau de propriétés contient une propriété à valeurs multiples avec aucune valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="1aee1-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1aee1-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="1aee1-125">Remarks</span></span>

<span data-ttu-id="1aee1-126">Si NULL est indiqué dans le paramètre de la _carte de circuit imprimé_ , la fonction **ScCountProps** valide le tableau des notifications, mais aucun décompte n’effectué.</span><span class="sxs-lookup"><span data-stu-id="1aee1-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="1aee1-127">Si une valeur non nulle est passée dans une _carte de circuit imprimé_, la fonction **ScCountNotifications** détermine la taille du tableau et stocke la cause la _carte de circuit imprimé_.</span><span class="sxs-lookup"><span data-stu-id="1aee1-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="1aee1-128">Le paramètre de la _carte de circuit imprimé_ doit être suffisant pour contenir l’intégralité du tableau.</span><span class="sxs-lookup"><span data-stu-id="1aee1-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="1aee1-129">Comme il est compté, **ScCountProps** valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="1aee1-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="1aee1-130">**ScCountProps** fonctionne uniquement avec les propriétés comporte des informations sur les MAPI.</span><span class="sxs-lookup"><span data-stu-id="1aee1-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1aee1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aee1-131">See also</span></span>



[<span data-ttu-id="1aee1-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="1aee1-132">PropCopyMore</span></span>](propcopymore.md)

