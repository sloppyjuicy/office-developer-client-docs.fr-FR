---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334880"
---
# <a name="fequalnames"></a><span data-ttu-id="f3510-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="f3510-103">FEqualNames</span></span>

  
  
<span data-ttu-id="f3510-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3510-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3510-105">Détermine si deux propriétés nommées MAPI sont identiques.</span><span class="sxs-lookup"><span data-stu-id="f3510-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3510-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f3510-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3510-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f3510-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f3510-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f3510-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3510-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3510-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3510-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f3510-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3510-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f3510-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="f3510-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3510-112">Parameters</span></span>

 <span data-ttu-id="f3510-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="f3510-113">_lpName1_</span></span>
  
> <span data-ttu-id="f3510-114">dans Pointeur vers une structure [MAPINAMEID](mapinameid.md) décrivant la première propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="f3510-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="f3510-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="f3510-115">_lpName2_</span></span>
  
> <span data-ttu-id="f3510-116">dans Pointeur vers une structure **MAPINAMEID** décrivant la deuxième propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="f3510-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3510-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3510-117">Return value</span></span>

<span data-ttu-id="f3510-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="f3510-118">TRUE</span></span> 
  
> <span data-ttu-id="f3510-119">Les deux noms de propriété sont égaux.</span><span class="sxs-lookup"><span data-stu-id="f3510-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="f3510-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="f3510-120">FALSE</span></span> 
  
> <span data-ttu-id="f3510-121">Les deux noms de propriété ne sont pas égaux.</span><span class="sxs-lookup"><span data-stu-id="f3510-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3510-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3510-122">Remarks</span></span>

<span data-ttu-id="f3510-123">La fonction **FEqualNames** est utile, car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété lui-même de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="f3510-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="f3510-124">Cela signifie que les deux structures ne peuvent pas être comparées par des méthodes binaires simples.</span><span class="sxs-lookup"><span data-stu-id="f3510-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="f3510-125">Le processus de test respecte la casse pour les chaînes de noms de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f3510-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

