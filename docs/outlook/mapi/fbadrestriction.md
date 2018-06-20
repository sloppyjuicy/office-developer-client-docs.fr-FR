---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783286"
---
# <a name="fbadrestriction"></a><span data-ttu-id="67e05-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="67e05-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="67e05-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67e05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67e05-105">Valide une restriction utilisée pour limiter un affichage de tableau.</span><span class="sxs-lookup"><span data-stu-id="67e05-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67e05-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="67e05-106">Header file:</span></span>  <br/> |<span data-ttu-id="67e05-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="67e05-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="67e05-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="67e05-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="67e05-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="67e05-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="67e05-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="67e05-110">Called by:</span></span>  <br/> |<span data-ttu-id="67e05-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="67e05-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="67e05-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67e05-112">Parameters</span></span>

 <span data-ttu-id="67e05-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="67e05-113">_lpres_</span></span>
  
> <span data-ttu-id="67e05-114">[in] Une structure [SRestriction](srestriction.md) définissant la restriction à valider.</span><span class="sxs-lookup"><span data-stu-id="67e05-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="67e05-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="67e05-115">Return value</span></span>

<span data-ttu-id="67e05-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="67e05-116">TRUE</span></span> 
  
> <span data-ttu-id="67e05-117">La restriction spécifiée, ou un ou plusieurs de ses subrestrictions, ne sont pas valide.</span><span class="sxs-lookup"><span data-stu-id="67e05-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="67e05-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="67e05-118">FALSE</span></span> 
  
> <span data-ttu-id="67e05-119">La restriction spécifiée et tous ses subrestrictions sont valides.</span><span class="sxs-lookup"><span data-stu-id="67e05-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67e05-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="67e05-120">Remarks</span></span>

<span data-ttu-id="67e05-121">Une fois une restriction est validée, il peut être passé dans les appels à la méthode [IMAPITable](imapitable-restrict.md) pour restreindre la table à certaines lignes, la méthode [IMAPITable::FindRow](imapitable-findrow.md) pour localiser une ligne de tableau et aux méthodes de l' [IMAPIContainer](imapicontainerimapiprop.md) interface pour effectuer une restriction sur un objet conteneur.</span><span class="sxs-lookup"><span data-stu-id="67e05-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

