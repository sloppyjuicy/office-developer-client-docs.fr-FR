---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590343"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="3b2a4-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="3b2a4-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="3b2a4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b2a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b2a4-105">Crée une structure nommée qui inclut une structure [DTBLBUTTON](dtblbutton.md) pour la description d’un bouton et une étiquette d’une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3b2a4-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b2a4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3b2a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b2a4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b2a4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3b2a4-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="3b2a4-108">Related structure:</span></span>  <br/> |<span data-ttu-id="3b2a4-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="3b2a4-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="3b2a4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b2a4-110">Parameters</span></span>

 <span data-ttu-id="3b2a4-111">_n_</span><span class="sxs-lookup"><span data-stu-id="3b2a4-111">_n_</span></span>
  
> <span data-ttu-id="3b2a4-112">Longueur de l’étiquette à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="3b2a4-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="3b2a4-113">_u_</span><span class="sxs-lookup"><span data-stu-id="3b2a4-113">_u_</span></span>
  
> <span data-ttu-id="3b2a4-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="3b2a4-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b2a4-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b2a4-115">Remarks</span></span>

<span data-ttu-id="3b2a4-116">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b2a4-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="3b2a4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b2a4-117">See also</span></span>



[<span data-ttu-id="3b2a4-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="3b2a4-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="3b2a4-119">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="3b2a4-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

