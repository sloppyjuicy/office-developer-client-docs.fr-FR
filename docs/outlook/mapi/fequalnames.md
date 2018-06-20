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
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783294"
---
# <a name="fequalnames"></a><span data-ttu-id="d9214-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="d9214-103">FEqualNames</span></span>

  
  
<span data-ttu-id="d9214-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9214-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9214-105">Détermine si les deux MAPI nommée des propriétés sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="d9214-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9214-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d9214-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9214-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d9214-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d9214-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="d9214-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9214-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9214-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d9214-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="d9214-110">Called by:</span></span>  <br/> |<span data-ttu-id="d9214-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d9214-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="d9214-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9214-112">Parameters</span></span>

 <span data-ttu-id="d9214-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="d9214-113">_lpName1_</span></span>
  
> <span data-ttu-id="d9214-114">[in] Pointeur vers une structure [MAPINAMEID](mapinameid.md) décrivant la première propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d9214-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="d9214-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="d9214-115">_lpName2_</span></span>
  
> <span data-ttu-id="d9214-116">[in] Pointeur vers une structure **MAPINAMEID** décrivant la seconde propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d9214-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9214-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d9214-117">Return value</span></span>

<span data-ttu-id="d9214-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="d9214-118">TRUE</span></span> 
  
> <span data-ttu-id="d9214-119">Les noms des deux propriétés sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="d9214-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="d9214-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="d9214-120">FALSE</span></span> 
  
> <span data-ttu-id="d9214-121">Les noms de deux propriété ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="d9214-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9214-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9214-122">Remarks</span></span>

<span data-ttu-id="d9214-123">La fonction **FEqualNames** est utile car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="d9214-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="d9214-124">Cela signifie que les deux structures ne peuvent être ouverts par les méthodes binaires simples.</span><span class="sxs-lookup"><span data-stu-id="d9214-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="d9214-125">Le processus de test respecte la casse pour les chaînes de nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="d9214-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

