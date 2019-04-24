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
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340963"
---
# <a name="fbadrestriction"></a><span data-ttu-id="bcebf-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="bcebf-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="bcebf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcebf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcebf-105">Valide une restriction utilisée pour limiter un affichage de tableau.</span><span class="sxs-lookup"><span data-stu-id="bcebf-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcebf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bcebf-106">Header file:</span></span>  <br/> |<span data-ttu-id="bcebf-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bcebf-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bcebf-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bcebf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bcebf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bcebf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bcebf-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bcebf-110">Called by:</span></span>  <br/> |<span data-ttu-id="bcebf-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bcebf-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="bcebf-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcebf-112">Parameters</span></span>

 <span data-ttu-id="bcebf-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="bcebf-113">_lpres_</span></span>
  
> <span data-ttu-id="bcebf-114">dans Structure [SRestriction](srestriction.md) définissant la restriction à valider.</span><span class="sxs-lookup"><span data-stu-id="bcebf-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bcebf-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bcebf-115">Return value</span></span>

<span data-ttu-id="bcebf-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="bcebf-116">TRUE</span></span> 
  
> <span data-ttu-id="bcebf-117">La restriction spécifiée, ou une ou plusieurs de ses sous-restrictions, n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bcebf-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="bcebf-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="bcebf-118">FALSE</span></span> 
  
> <span data-ttu-id="bcebf-119">La restriction spécifiée et toutes ses sous-restrictions sont valides.</span><span class="sxs-lookup"><span data-stu-id="bcebf-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcebf-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="bcebf-120">Remarks</span></span>

<span data-ttu-id="bcebf-121">Une fois qu'une restriction est validée, elle peut être transmise dans les appels à la méthode [IMAPITable:: Restrict](imapitable-restrict.md) pour limiter la table à certaines lignes, jusqu'à la méthode [IMAPITable:: FindRow](imapitable-findrow.md) pour localiser une ligne de table et aux méthodes de [IMAPIContainer](imapicontainerimapiprop.md) interface permettant d'effectuer une restriction sur un objet Container.</span><span class="sxs-lookup"><span data-stu-id="bcebf-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

