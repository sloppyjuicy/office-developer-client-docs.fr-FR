---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438392"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="8d664-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="8d664-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="8d664-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d664-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d664-105">Décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8d664-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d664-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8d664-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d664-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d664-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8d664-108">Macro associée :</span><span class="sxs-lookup"><span data-stu-id="8d664-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="8d664-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="8d664-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="8d664-110">Members</span><span class="sxs-lookup"><span data-stu-id="8d664-110">Members</span></span>

 <span data-ttu-id="8d664-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="8d664-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="8d664-112">Position en mémoire de la chaîne de caractères qui accompagne la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="8d664-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="8d664-113">S’il est affiché, l’étiquette apparaît en haut, à gauche de la zone.</span><span class="sxs-lookup"><span data-stu-id="8d664-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="8d664-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="8d664-114">**ulFlags**</span></span>
  
> <span data-ttu-id="8d664-115">Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="8d664-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="8d664-116">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="8d664-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="8d664-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d664-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8d664-118">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d664-118">The label is in Unicode format.</span></span> <span data-ttu-id="8d664-119">Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="8d664-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d664-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d664-120">Remarks</span></span>

<span data-ttu-id="8d664-121">Une structure **DTBLGROUPBOX** décrit un contrôle de zone de groupe utilisé pour associer visuellement d’autres contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8d664-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="8d664-122">La technique de mise en surbrillance implique d’entourer les autres contrôles d’une zone.</span><span class="sxs-lookup"><span data-stu-id="8d664-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="8d664-123">Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="8d664-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="8d664-124">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="8d664-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d664-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d664-125">See also</span></span>



[<span data-ttu-id="8d664-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="8d664-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="8d664-127">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8d664-127">MAPI Structures</span></span>](mapi-structures.md)

