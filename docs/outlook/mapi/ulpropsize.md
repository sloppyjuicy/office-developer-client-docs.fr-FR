---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416901"
---
# <a name="ulpropsize"></a><span data-ttu-id="7df87-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="7df87-103">UlPropSize</span></span>

  
  
<span data-ttu-id="7df87-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7df87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7df87-105">Renvoie la taille d'une seule valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="7df87-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7df87-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7df87-106">Header file:</span></span>  <br/> |<span data-ttu-id="7df87-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7df87-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7df87-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7df87-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7df87-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7df87-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7df87-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7df87-110">Called by:</span></span>  <br/> |<span data-ttu-id="7df87-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7df87-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="7df87-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7df87-112">Parameters</span></span>

 <span data-ttu-id="7df87-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="7df87-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="7df87-114">dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la propriété à mesurer.</span><span class="sxs-lookup"><span data-stu-id="7df87-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7df87-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7df87-115">Return value</span></span>

<span data-ttu-id="7df87-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7df87-116">S_OK</span></span> 
  
> <span data-ttu-id="7df87-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="7df87-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7df87-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7df87-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7df87-119">Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="7df87-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7df87-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7df87-120">Remarks</span></span>

<span data-ttu-id="7df87-121">La fonction **UlPropSize** renvoie la taille en octets de la valeur de la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7df87-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="7df87-122">Il ignore la taille du reste de la structure **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="7df87-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

