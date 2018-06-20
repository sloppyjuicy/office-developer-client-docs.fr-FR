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
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783275"
---
# <a name="fbadentrylist"></a><span data-ttu-id="604b6-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="604b6-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="604b6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="604b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="604b6-105">Valide une liste d’identificateurs d’entrée MAPI.</span><span class="sxs-lookup"><span data-stu-id="604b6-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="604b6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="604b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="604b6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="604b6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="604b6-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="604b6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="604b6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="604b6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="604b6-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="604b6-110">Called by:</span></span>  <br/> |<span data-ttu-id="604b6-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="604b6-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="604b6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="604b6-112">Parameters</span></span>

 <span data-ttu-id="604b6-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="604b6-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="604b6-114">[in] Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient un tableau d’identificateurs d’entrée à valider.</span><span class="sxs-lookup"><span data-stu-id="604b6-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="604b6-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="604b6-115">Return value</span></span>

<span data-ttu-id="604b6-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="604b6-116">TRUE</span></span> 
  
> <span data-ttu-id="604b6-117">Un ou plusieurs des identificateurs d’entrée répertoriés ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="604b6-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="604b6-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="604b6-118">FALSE</span></span> 
  
> <span data-ttu-id="604b6-119">Tous les identificateurs d’entrée répertoriés sont valides.</span><span class="sxs-lookup"><span data-stu-id="604b6-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="604b6-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="604b6-120">Remarks</span></span>

<span data-ttu-id="604b6-121">La fonction **FBadEntryList** détermine si la liste Identificateur d’entrée a été correctement générée.</span><span class="sxs-lookup"><span data-stu-id="604b6-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="604b6-122">Un exemple d’un identificateur non valide est 1 qui a été incorrectement allouer de la mémoire ou un identificateur pour une taille incorrecte.</span><span class="sxs-lookup"><span data-stu-id="604b6-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

