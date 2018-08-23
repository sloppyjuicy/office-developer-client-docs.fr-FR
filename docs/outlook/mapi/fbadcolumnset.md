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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575097"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="a49a8-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="a49a8-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="a49a8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a49a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a49a8-105">La validité d’une colonne de table définie pour les tests utilisent par un fournisseur de services dans un appel suivant à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="a49a8-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a49a8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a49a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a49a8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a49a8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a49a8-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a49a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a49a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a49a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a49a8-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a49a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a49a8-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a49a8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="a49a8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a49a8-112">Parameters</span></span>

 <span data-ttu-id="a49a8-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="a49a8-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="a49a8-114">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété définir les colonnes de la table à valider.</span><span class="sxs-lookup"><span data-stu-id="a49a8-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a49a8-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a49a8-115">Return value</span></span>

<span data-ttu-id="a49a8-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="a49a8-116">TRUE</span></span> 
  
> <span data-ttu-id="a49a8-117">L’ensemble de la colonne spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a49a8-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="a49a8-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="a49a8-118">FALSE</span></span> 
  
> <span data-ttu-id="a49a8-119">L’ensemble de la colonne spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="a49a8-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a49a8-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="a49a8-120">Remarks</span></span>

<span data-ttu-id="a49a8-121">La fonction **FBadColumnSet** traite les colonnes du type PT_ERROR comme non valide et les colonnes du type PT_NULL comme étant valide.</span><span class="sxs-lookup"><span data-stu-id="a49a8-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

