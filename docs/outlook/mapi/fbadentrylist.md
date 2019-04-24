---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341068"
---
# <a name="fbadentrylist"></a><span data-ttu-id="fd27a-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="fd27a-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="fd27a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd27a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd27a-105">Valide une liste d'identificateurs d'entrée MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd27a-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd27a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fd27a-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd27a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="fd27a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="fd27a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="fd27a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fd27a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fd27a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fd27a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="fd27a-110">Called by:</span></span>  <br/> |<span data-ttu-id="fd27a-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fd27a-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="fd27a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd27a-112">Parameters</span></span>

 <span data-ttu-id="fd27a-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="fd27a-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="fd27a-114">dans Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient un tableau d'identificateurs d'entrée à valider.</span><span class="sxs-lookup"><span data-stu-id="fd27a-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fd27a-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd27a-115">Return value</span></span>

<span data-ttu-id="fd27a-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="fd27a-116">TRUE</span></span> 
  
> <span data-ttu-id="fd27a-117">Un ou plusieurs des identificateurs d'entrée répertoriés ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="fd27a-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="fd27a-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd27a-118">FALSE</span></span> 
  
> <span data-ttu-id="fd27a-119">Tous les identificateurs d'entrée répertoriés sont valides.</span><span class="sxs-lookup"><span data-stu-id="fd27a-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd27a-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd27a-120">Remarks</span></span>

<span data-ttu-id="fd27a-121">La fonction **FBadEntryList** détermine si la liste d'identificateurs d'entrée a été correctement générée.</span><span class="sxs-lookup"><span data-stu-id="fd27a-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="fd27a-122">Un exemple d'identificateur non valide est celui pour lequel la mémoire a été incorrectement allouée ou un identificateur de taille incorrecte.</span><span class="sxs-lookup"><span data-stu-id="fd27a-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

