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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787183"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="9bc72-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="9bc72-103">SizedDtblLabel</span></span>

<span data-ttu-id="9bc72-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bc72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bc72-105">Crée une structure nommée qui inclut une structure [DTBLLABEL](dtbllabel.md) pour la description d’un contrôle label et l’étiquette associé d’une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9bc72-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bc72-106">Spécifié dans le fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9bc72-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="9bc72-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bc72-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9bc72-108">Structure connexe</span><span class="sxs-lookup"><span data-stu-id="9bc72-108">Related structure</span></span>  <br/> |<span data-ttu-id="9bc72-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="9bc72-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="9bc72-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bc72-110">Parameters</span></span>

<span data-ttu-id="9bc72-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9bc72-111">_n_</span></span>
  
> <span data-ttu-id="9bc72-112">Longueur de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="9bc72-112">Length of the label.</span></span> <span data-ttu-id="9bc72-113">Cela inclut le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="9bc72-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="9bc72-114">_u_</span><span class="sxs-lookup"><span data-stu-id="9bc72-114">_u_</span></span>
  
> <span data-ttu-id="9bc72-115">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="9bc72-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9bc72-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9bc72-116">Remarks</span></span>

<span data-ttu-id="9bc72-117">La macro **SizedDtblLabel** vous permet de définir une étiquette d’affichage tableau lorsque le nombre de caractères dans l’étiquette est connu.</span><span class="sxs-lookup"><span data-stu-id="9bc72-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="9bc72-118">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9bc72-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="9bc72-119">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblLabel** comme un pointeur de structure **DTBLLABEL** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="9bc72-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="9bc72-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bc72-120">See also</span></span>

- [<span data-ttu-id="9bc72-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="9bc72-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="9bc72-122">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="9bc72-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

