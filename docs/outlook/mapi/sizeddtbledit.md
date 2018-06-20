---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787166"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="73f0f-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="73f0f-103">SizedDtblEdit</span></span>

<span data-ttu-id="73f0f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73f0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73f0f-105">Crée une structure nommée qui inclut une structure [DTBLEDIT](dtbledit.md) pour la description d’un contrôle d’édition et le nombre maximal de caractères pouvant être entré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="73f0f-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73f0f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="73f0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="73f0f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73f0f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="73f0f-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="73f0f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="73f0f-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="73f0f-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="73f0f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73f0f-110">Parameters</span></span>

<span data-ttu-id="73f0f-111">_n_</span><span class="sxs-lookup"><span data-stu-id="73f0f-111">_n_</span></span>
  
> <span data-ttu-id="73f0f-112">Nombre maximal de caractères pouvant être entré dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="73f0f-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="73f0f-113">_u_</span><span class="sxs-lookup"><span data-stu-id="73f0f-113">_u_</span></span>
  
> <span data-ttu-id="73f0f-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="73f0f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73f0f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="73f0f-115">Remarks</span></span>

<span data-ttu-id="73f0f-116">La macro **SizedDtblEdit** vous permet de définir un contrôle d’édition lorsque le nombre de caractères activés est connu.</span><span class="sxs-lookup"><span data-stu-id="73f0f-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="73f0f-117">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="73f0f-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="73f0f-118">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblEdit** comme un pointeur de structure **DTBLEDIT** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="73f0f-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="73f0f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73f0f-119">See also</span></span>

- [<span data-ttu-id="73f0f-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="73f0f-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="73f0f-121">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="73f0f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

