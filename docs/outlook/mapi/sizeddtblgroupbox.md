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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282732"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="9b05c-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="9b05c-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="9b05c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b05c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b05c-105">Crée une structure nommée qui inclut une structure [DTBLGROUPBOX](dtblgroupbox.md) pour la description d'un contrôle de zone de groupe et une étiquette d'une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b05c-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b05c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9b05c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b05c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9b05c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9b05c-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="9b05c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9b05c-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="9b05c-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="9b05c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b05c-110">Parameters</span></span>

<span data-ttu-id="9b05c-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9b05c-111">_n_</span></span>
  
> <span data-ttu-id="9b05c-112">Longueur de l'étiquette de la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="9b05c-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="9b05c-113">_u_</span><span class="sxs-lookup"><span data-stu-id="9b05c-113">_u_</span></span>
  
> <span data-ttu-id="9b05c-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="9b05c-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b05c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="9b05c-115">Remarks</span></span>

<span data-ttu-id="9b05c-116">La macro **SizedDtblGroupBox** vous permet de définir un contrôle de zone de groupe lorsque la longueur de l'étiquette est connue.</span><span class="sxs-lookup"><span data-stu-id="9b05c-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="9b05c-117">La nouvelle structure est créée avec les membres suivants:</span><span class="sxs-lookup"><span data-stu-id="9b05c-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="9b05c-118">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblGroupBox** en tant que pointeur de structure **DTBLGROUPBOX** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="9b05c-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="9b05c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b05c-119">See also</span></span>

- [<span data-ttu-id="9b05c-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="9b05c-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="9b05c-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="9b05c-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

