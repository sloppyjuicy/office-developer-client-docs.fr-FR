---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408613"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="807b5-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="807b5-103">SizedDtblLabel</span></span>

<span data-ttu-id="807b5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="807b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="807b5-105">Crée une structure nommée qui inclut une structure [DTBLLABEL](dtbllabel.md) pour décrire un contrôle d’étiquette et l’étiquette associée d’une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="807b5-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="807b5-106">Spécifié dans le fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="807b5-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="807b5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="807b5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="807b5-108">Structure connexe</span><span class="sxs-lookup"><span data-stu-id="807b5-108">Related structure</span></span>  <br/> |<span data-ttu-id="807b5-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="807b5-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="807b5-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="807b5-110">Parameters</span></span>

<span data-ttu-id="807b5-111">_n_</span><span class="sxs-lookup"><span data-stu-id="807b5-111">_n_</span></span>
  
> <span data-ttu-id="807b5-112">Longueur de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="807b5-112">Length of the label.</span></span> <span data-ttu-id="807b5-113">Cela inclut le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="807b5-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="807b5-114">_u_</span><span class="sxs-lookup"><span data-stu-id="807b5-114">_u_</span></span>
  
> <span data-ttu-id="807b5-115">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="807b5-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="807b5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="807b5-116">Remarks</span></span>

<span data-ttu-id="807b5-117">La macro **SizedDtblLabel** vous permet de définir une étiquette de tableau d’affichage lorsque le nombre de caractères de l’étiquette est connu.</span><span class="sxs-lookup"><span data-stu-id="807b5-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="807b5-118">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="807b5-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="807b5-119">Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblLabel** en tant que pointeur de structure **DTBLLABEL,** effectuez la distribution suivante :</span><span class="sxs-lookup"><span data-stu-id="807b5-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="807b5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="807b5-120">See also</span></span>

- [<span data-ttu-id="807b5-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="807b5-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="807b5-122">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="807b5-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

