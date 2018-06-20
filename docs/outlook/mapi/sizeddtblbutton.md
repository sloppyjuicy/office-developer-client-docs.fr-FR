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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787159"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="13422-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="13422-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="13422-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13422-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13422-105">Crée une structure nommée qui inclut une structure [DTBLBUTTON](dtblbutton.md) pour la description d’un bouton et une étiquette d’une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="13422-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13422-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="13422-106">Header file:</span></span>  <br/> |<span data-ttu-id="13422-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13422-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="13422-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="13422-108">Related structure:</span></span>  <br/> |<span data-ttu-id="13422-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="13422-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="13422-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13422-110">Parameters</span></span>

 <span data-ttu-id="13422-111">_n_</span><span class="sxs-lookup"><span data-stu-id="13422-111">_n_</span></span>
  
> <span data-ttu-id="13422-112">Longueur de l’étiquette à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="13422-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="13422-113">_u_</span><span class="sxs-lookup"><span data-stu-id="13422-113">_u_</span></span>
  
> <span data-ttu-id="13422-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="13422-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13422-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="13422-115">Remarks</span></span>

<span data-ttu-id="13422-116">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="13422-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="13422-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13422-117">See also</span></span>



[<span data-ttu-id="13422-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="13422-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="13422-119">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="13422-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

