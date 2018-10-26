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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570848"
---
# <a name="fequalnames"></a><span data-ttu-id="a85b8-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="a85b8-103">FEqualNames</span></span>

  
  
<span data-ttu-id="a85b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a85b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a85b8-105">Détermine si les deux MAPI nommée des propriétés sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="a85b8-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a85b8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a85b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a85b8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a85b8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a85b8-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a85b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a85b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a85b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a85b8-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a85b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a85b8-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a85b8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="a85b8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a85b8-112">Parameters</span></span>

 <span data-ttu-id="a85b8-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="a85b8-113">_lpName1_</span></span>
  
> <span data-ttu-id="a85b8-114">[in] Pointeur vers une structure [MAPINAMEID](mapinameid.md) décrivant la première propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="a85b8-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="a85b8-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="a85b8-115">_lpName2_</span></span>
  
> <span data-ttu-id="a85b8-116">[in] Pointeur vers une structure **MAPINAMEID** décrivant la seconde propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="a85b8-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a85b8-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a85b8-117">Return value</span></span>

<span data-ttu-id="a85b8-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="a85b8-118">TRUE</span></span> 
  
> <span data-ttu-id="a85b8-119">Les noms des deux propriétés sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="a85b8-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="a85b8-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="a85b8-120">FALSE</span></span> 
  
> <span data-ttu-id="a85b8-121">Les noms de deux propriété ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="a85b8-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a85b8-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="a85b8-122">Remarks</span></span>

<span data-ttu-id="a85b8-123">La fonction **FEqualNames** est utile car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="a85b8-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="a85b8-124">Cela signifie que les deux structures ne peuvent être ouverts par les méthodes binaires simples.</span><span class="sxs-lookup"><span data-stu-id="a85b8-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="a85b8-125">Le processus de test respecte la casse pour les chaînes de nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="a85b8-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

