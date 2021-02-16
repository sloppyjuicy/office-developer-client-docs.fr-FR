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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417657"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="50c38-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="50c38-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="50c38-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c38-105">Définit ou modifie la valeur d’une propriété unique sur une interface de propriétés, c’est-à-dire une interface dérivée [d’IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="50c38-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50c38-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="50c38-106">Header file:</span></span>  <br/> |<span data-ttu-id="50c38-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="50c38-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="50c38-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="50c38-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="50c38-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="50c38-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="50c38-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="50c38-110">Called by:</span></span>  <br/> |<span data-ttu-id="50c38-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="50c38-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="50c38-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50c38-112">Parameters</span></span>

 <span data-ttu-id="50c38-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="50c38-113">_pmp_</span></span>
  
> <span data-ttu-id="50c38-114">[in] Pointeur vers une interface [IMAPIProp](imapipropiunknown.md) sur laquelle la valeur de la propriété doit être définie ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="50c38-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="50c38-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="50c38-115">_pprop_</span></span>
  
> <span data-ttu-id="50c38-116">[in] Pointeur vers la structure [SPropValue](spropvalue.md) définissant la valeur à définir sur la _propriété pmp._</span><span class="sxs-lookup"><span data-stu-id="50c38-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="50c38-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50c38-117">Return value</span></span>

<span data-ttu-id="50c38-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="50c38-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50c38-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="50c38-119">Remarks</span></span>

<span data-ttu-id="50c38-120">Contrairement à [la méthode IMAPIProp::SetProps,](imapiprop-setprops.md) la fonction **HrSetOneProp** ne renvoie jamais d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="50c38-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="50c38-121">Étant donné qu’elle ne définit qu’une seule propriété, elle réussit ou échoue simplement.</span><span class="sxs-lookup"><span data-stu-id="50c38-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="50c38-122">Pour définir ou modifier plusieurs propriétés, **SetProps** est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="50c38-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="50c38-123">Vous pouvez récupérer une propriété unique avec [la fonction HrGetOneProp.](hrgetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="50c38-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

