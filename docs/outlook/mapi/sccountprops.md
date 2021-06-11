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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404973"
---
# <a name="sccountprops"></a><span data-ttu-id="871b4-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="871b4-103">ScCountProps</span></span>

  
  
<span data-ttu-id="871b4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="871b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="871b4-105">Détermine la taille, en octets, d’un tableau de valeurs de propriétés et valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="871b4-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="871b4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="871b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="871b4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="871b4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="871b4-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="871b4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="871b4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="871b4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="871b4-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="871b4-110">Called by:</span></span>  <br/> |<span data-ttu-id="871b4-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="871b4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="871b4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="871b4-112">Parameters</span></span>

 <span data-ttu-id="871b4-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="871b4-113">_cprop_</span></span>
  
> <span data-ttu-id="871b4-114">[in] Nombre de propriétés dans le tableau indiqué par le _paramètre rgprop._</span><span class="sxs-lookup"><span data-stu-id="871b4-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="871b4-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="871b4-115">_rgprop_</span></span>
  
> <span data-ttu-id="871b4-116">[in] Pointeur vers une plage dans un tableau de structures [SPropValue](spropvalue.md) qui définit les propriétés dont la taille doit être déterminée.</span><span class="sxs-lookup"><span data-stu-id="871b4-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="871b4-117">Cette plage ne commence pas nécessairement au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="871b4-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="871b4-118">_pcb_</span><span class="sxs-lookup"><span data-stu-id="871b4-118">_pcb_</span></span>
  
> <span data-ttu-id="871b4-119">[out] Pointeur facultatif vers la taille, en octets, du tableau de propriétés.</span><span class="sxs-lookup"><span data-stu-id="871b4-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="871b4-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="871b4-120">Return value</span></span>

<span data-ttu-id="871b4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="871b4-121">S_OK</span></span> 
  
> <span data-ttu-id="871b4-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="871b4-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="871b4-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="871b4-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="871b4-124">Au moins une propriété du tableau de valeurs de propriétés possède un identificateur PROP_ID_NULL ou PROP_ID_INVALID, ou le tableau de propriétés contient une propriété à valeurs multiples sans valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="871b4-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="871b4-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="871b4-125">Remarks</span></span>

<span data-ttu-id="871b4-126">Si NULL est transmis dans le  _paramètre pcb,_ la **fonction ScCountProps** valide le tableau de notifications, mais aucun décompte n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="871b4-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="871b4-127">Si une valeur non null est passée dans  _pcb,_ la **fonction ScCountNotifications** détermine la taille du tableau et stocke la  _cause pcb_.</span><span class="sxs-lookup"><span data-stu-id="871b4-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="871b4-128">Le  _paramètre pcb_ doit être suffisamment grand pour contenir la totalité du tableau.</span><span class="sxs-lookup"><span data-stu-id="871b4-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="871b4-129">Au cours de son comptage, **ScCountProps** valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="871b4-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="871b4-130">**ScCountProps fonctionne** uniquement avec les propriétés sur lesquelles MAPI dispose d’informations.</span><span class="sxs-lookup"><span data-stu-id="871b4-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="871b4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="871b4-131">See also</span></span>



[<span data-ttu-id="871b4-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="871b4-132">PropCopyMore</span></span>](propcopymore.md)

