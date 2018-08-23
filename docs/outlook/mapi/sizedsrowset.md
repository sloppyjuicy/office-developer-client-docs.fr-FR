---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583938"
---
# <a name="sizedsrowset"></a><span data-ttu-id="91617-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="91617-103">SizedSRowSet</span></span>

<span data-ttu-id="91617-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91617-105">Crée une structure [SRowSet](srowset.md) nommée qui contient un nombre spécifié de lignes.</span><span class="sxs-lookup"><span data-stu-id="91617-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91617-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="91617-106">Header file:</span></span>  <br/> |<span data-ttu-id="91617-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91617-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="91617-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="91617-108">Related structure:</span></span>  <br/> |<span data-ttu-id="91617-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="91617-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="91617-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91617-110">Parameters</span></span>

<span data-ttu-id="91617-111">__a_</span><span class="sxs-lookup"><span data-stu-id="91617-111">__crow_</span></span>
  
> <span data-ttu-id="91617-112">Comptage du nombre de lignes à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="91617-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="91617-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="91617-113">__name_</span></span>
  
> <span data-ttu-id="91617-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="91617-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91617-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="91617-115">Remarks</span></span>

<span data-ttu-id="91617-116">Pour utiliser la nouvelle structure de résultats de la macro **SizedSRowSet** comme un pointeur vers une structure **SRowSet** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="91617-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="91617-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91617-117">See also</span></span>

- [<span data-ttu-id="91617-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="91617-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="91617-119">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="91617-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

