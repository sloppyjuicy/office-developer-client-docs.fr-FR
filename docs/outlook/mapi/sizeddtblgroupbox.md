---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419316"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="be93e-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="be93e-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="be93e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be93e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be93e-105">Crée une structure nommée qui inclut une structure [DTBLGROUPBOX](dtblgroupbox.md) pour décrire un contrôle de zone de groupe et une étiquette d’une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="be93e-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be93e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="be93e-106">Header file:</span></span>  <br/> |<span data-ttu-id="be93e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be93e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="be93e-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="be93e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="be93e-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="be93e-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="be93e-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="be93e-110">Parameters</span></span>

<span data-ttu-id="be93e-111">_n_</span><span class="sxs-lookup"><span data-stu-id="be93e-111">_n_</span></span>
  
> <span data-ttu-id="be93e-112">Longueur de l’étiquette de la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="be93e-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="be93e-113">_u_</span><span class="sxs-lookup"><span data-stu-id="be93e-113">_u_</span></span>
  
> <span data-ttu-id="be93e-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="be93e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be93e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="be93e-115">Remarks</span></span>

<span data-ttu-id="be93e-116">La macro **SizedDtblGroupBox** vous permet de définir un contrôle de zone de groupe lorsque la longueur de l’étiquette est connue.</span><span class="sxs-lookup"><span data-stu-id="be93e-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="be93e-117">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be93e-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="be93e-118">Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblGroupBox** en tant que pointeur de structure **DTBLGROUPBOX,** effectuez la distribution suivante :</span><span class="sxs-lookup"><span data-stu-id="be93e-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="be93e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be93e-119">See also</span></span>

- [<span data-ttu-id="be93e-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="be93e-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="be93e-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="be93e-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

