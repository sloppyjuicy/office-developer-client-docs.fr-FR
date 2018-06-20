---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783566"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="d2cea-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="d2cea-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="d2cea-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2cea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2cea-105">Définit ou modifie la valeur d’une seule propriété sur une interface de propriété, autrement dit, une interface dérivée de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d2cea-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2cea-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d2cea-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2cea-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d2cea-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d2cea-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="d2cea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2cea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2cea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2cea-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="d2cea-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2cea-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d2cea-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="d2cea-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2cea-112">Parameters</span></span>

 <span data-ttu-id="d2cea-113">_nous procure_</span><span class="sxs-lookup"><span data-stu-id="d2cea-113">_pmp_</span></span>
  
> <span data-ttu-id="d2cea-114">[in] Pointeur vers une interface [IMAPIProp](imapipropiunknown.md) sur lequel la valeur de la propriété doit être défini ou modifié.</span><span class="sxs-lookup"><span data-stu-id="d2cea-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="d2cea-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="d2cea-115">_pprop_</span></span>
  
> <span data-ttu-id="d2cea-116">[in] Pointeur vers la structure [SPropValue](spropvalue.md) définissant la valeur à définir la propriété _nous procure_ .</span><span class="sxs-lookup"><span data-stu-id="d2cea-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d2cea-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2cea-117">Return value</span></span>

<span data-ttu-id="d2cea-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d2cea-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2cea-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2cea-119">Remarks</span></span>

<span data-ttu-id="d2cea-120">Contrairement à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) , la fonction **HrSetOneProp** ne retourne jamais les éventuels avertissements.</span><span class="sxs-lookup"><span data-stu-id="d2cea-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="d2cea-121">Parce qu’elle ne définit qu’une seule propriété, il suffit réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="d2cea-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="d2cea-122">Pour définir ou modifier plusieurs propriétés, **SetProps** est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="d2cea-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="d2cea-123">Vous pouvez récupérer une seule propriété avec la fonction [HrGetOneProp](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="d2cea-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

