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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591659"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="a2fed-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="a2fed-103">SizedDtblEdit</span></span>

<span data-ttu-id="a2fed-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2fed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2fed-105">Crée une structure nommée qui inclut une structure [DTBLEDIT](dtbledit.md) pour la description d’un contrôle d’édition et le nombre maximal de caractères pouvant être entré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="a2fed-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2fed-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a2fed-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2fed-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2fed-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a2fed-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="a2fed-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a2fed-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="a2fed-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="a2fed-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2fed-110">Parameters</span></span>

<span data-ttu-id="a2fed-111">_n_</span><span class="sxs-lookup"><span data-stu-id="a2fed-111">_n_</span></span>
  
> <span data-ttu-id="a2fed-112">Nombre maximal de caractères pouvant être entré dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="a2fed-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="a2fed-113">_u_</span><span class="sxs-lookup"><span data-stu-id="a2fed-113">_u_</span></span>
  
> <span data-ttu-id="a2fed-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="a2fed-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2fed-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2fed-115">Remarks</span></span>

<span data-ttu-id="a2fed-116">La macro **SizedDtblEdit** vous permet de définir un contrôle d’édition lorsque le nombre de caractères activés est connu.</span><span class="sxs-lookup"><span data-stu-id="a2fed-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="a2fed-117">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2fed-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="a2fed-118">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblEdit** comme un pointeur de structure **DTBLEDIT** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="a2fed-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="a2fed-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2fed-119">See also</span></span>

- [<span data-ttu-id="a2fed-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="a2fed-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="a2fed-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="a2fed-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

