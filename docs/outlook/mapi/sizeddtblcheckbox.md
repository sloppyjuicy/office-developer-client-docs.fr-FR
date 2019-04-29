---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420807"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="c21e6-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="c21e6-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="c21e6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c21e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c21e6-105">Crée une structure nommée qui inclut une structure [DTBLCHECKBOX](dtblcheckbox.md) pour la description d'un contrôle case à cocher et une étiquette d'une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c21e6-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c21e6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c21e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="c21e6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c21e6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c21e6-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="c21e6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c21e6-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="c21e6-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="c21e6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c21e6-110">Parameters</span></span>

<span data-ttu-id="c21e6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="c21e6-111">_n_</span></span>
  
> <span data-ttu-id="c21e6-112">Longueur de l'étiquette à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="c21e6-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="c21e6-113">_u_</span><span class="sxs-lookup"><span data-stu-id="c21e6-113">_u_</span></span>
  
> <span data-ttu-id="c21e6-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="c21e6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c21e6-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c21e6-115">Remarks</span></span>

<span data-ttu-id="c21e6-116">La macro **SizedDtblCheckBox** vous permet de définir une case à cocher lorsque le nombre de caractères d'étiquette est connu.</span><span class="sxs-lookup"><span data-stu-id="c21e6-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="c21e6-117">La nouvelle structure est créée avec les membres suivants:</span><span class="sxs-lookup"><span data-stu-id="c21e6-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="c21e6-118">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblCheckBox** en tant que pointeur de structure **DTBLCHECKBOX** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="c21e6-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="c21e6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c21e6-119">See also</span></span>

- [<span data-ttu-id="c21e6-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="c21e6-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="c21e6-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="c21e6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

