---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434717"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="9a95e-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="9a95e-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="9a95e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a95e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a95e-105">Teste la validité d’un ensemble de colonnes de tableau à utiliser par un fournisseur de services dans un appel ultérieur à la méthode [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="9a95e-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a95e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9a95e-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a95e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9a95e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9a95e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="9a95e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a95e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9a95e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9a95e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="9a95e-110">Called by:</span></span>  <br/> |<span data-ttu-id="9a95e-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="9a95e-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="9a95e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a95e-112">Parameters</span></span>

 <span data-ttu-id="9a95e-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="9a95e-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="9a95e-114">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété définissant les colonnes de tableau à valider.</span><span class="sxs-lookup"><span data-stu-id="9a95e-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9a95e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a95e-115">Return value</span></span>

<span data-ttu-id="9a95e-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="9a95e-116">TRUE</span></span> 
  
> <span data-ttu-id="9a95e-117">Le jeu de colonnes spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9a95e-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="9a95e-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a95e-118">FALSE</span></span> 
  
> <span data-ttu-id="9a95e-119">Le jeu de colonnes spécifié est valide.</span><span class="sxs-lookup"><span data-stu-id="9a95e-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a95e-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a95e-120">Remarks</span></span>

<span data-ttu-id="9a95e-121">La **fonction FBadColumnSet** traite les colonnes de type PT_ERROR comme non valides et les colonnes de type PT_NULL comme valides.</span><span class="sxs-lookup"><span data-stu-id="9a95e-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

