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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2bfe2841592987c530f6323db94834c1dcb64b2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576637"
---
# <a name="ulpropsize"></a><span data-ttu-id="7a49d-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="7a49d-103">UlPropSize</span></span>

  
  
<span data-ttu-id="7a49d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a49d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a49d-105">Retourne la taille d’une seule valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="7a49d-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a49d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7a49d-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a49d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a49d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7a49d-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="7a49d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7a49d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7a49d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7a49d-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="7a49d-110">Called by:</span></span>  <br/> |<span data-ttu-id="7a49d-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7a49d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="7a49d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a49d-112">Parameters</span></span>

 <span data-ttu-id="7a49d-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="7a49d-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="7a49d-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définit la propriété à mesurer.</span><span class="sxs-lookup"><span data-stu-id="7a49d-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7a49d-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7a49d-115">Return value</span></span>

<span data-ttu-id="7a49d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a49d-116">S_OK</span></span> 
  
> <span data-ttu-id="7a49d-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="7a49d-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7a49d-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7a49d-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7a49d-119">Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="7a49d-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a49d-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a49d-120">Remarks</span></span>

<span data-ttu-id="7a49d-121">La fonction **UlPropSize** retourne la taille, en octets, de la valeur de propriété pour la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7a49d-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="7a49d-122">Elle ignore la taille du reste de la structure **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="7a49d-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

