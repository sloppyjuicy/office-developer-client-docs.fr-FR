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
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282704"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="b232e-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="b232e-103">SizedDtblLabel</span></span>

<span data-ttu-id="b232e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b232e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b232e-105">Crée une structure nommée qui inclut une structure [DTBLLABEL](dtbllabel.md) pour la description d'un contrôle Label et de l'étiquette associée d'une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b232e-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b232e-106">Spécifié dans le fichier d'en-tête:</span><span class="sxs-lookup"><span data-stu-id="b232e-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="b232e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b232e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b232e-108">Structure associée</span><span class="sxs-lookup"><span data-stu-id="b232e-108">Related structure</span></span>  <br/> |<span data-ttu-id="b232e-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="b232e-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="b232e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b232e-110">Parameters</span></span>

<span data-ttu-id="b232e-111">_n_</span><span class="sxs-lookup"><span data-stu-id="b232e-111">_n_</span></span>
  
> <span data-ttu-id="b232e-112">Longueur de l'étiquette.</span><span class="sxs-lookup"><span data-stu-id="b232e-112">Length of the label.</span></span> <span data-ttu-id="b232e-113">Cela inclut le caractère de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="b232e-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="b232e-114">_u_</span><span class="sxs-lookup"><span data-stu-id="b232e-114">_u_</span></span>
  
> <span data-ttu-id="b232e-115">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="b232e-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b232e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b232e-116">Remarks</span></span>

<span data-ttu-id="b232e-117">La macro **SizedDtblLabel** vous permet de définir une étiquette de tableau d'affichage lorsque le nombre de caractères dans l'étiquette est connu.</span><span class="sxs-lookup"><span data-stu-id="b232e-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="b232e-118">La nouvelle structure est créée avec les membres suivants:</span><span class="sxs-lookup"><span data-stu-id="b232e-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="b232e-119">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblLabel** en tant que pointeur de structure **DTBLLABEL** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="b232e-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="b232e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b232e-120">See also</span></span>

- [<span data-ttu-id="b232e-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="b232e-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="b232e-122">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="b232e-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

