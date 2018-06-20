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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9295c37a46d3566089f708aaaa0b9fc3b5f30db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783232"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="e1de0-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="e1de0-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="e1de0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1de0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1de0-105">Décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e1de0-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1de0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e1de0-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1de0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1de0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e1de0-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="e1de0-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e1de0-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="e1de0-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="e1de0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e1de0-110">Members</span></span>

 <span data-ttu-id="e1de0-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="e1de0-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="e1de0-112">Position dans la mémoire de la chaîne de caractères qui accompagne la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="e1de0-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="e1de0-113">Si affiché, l’étiquette s’affiche sur le côté supérieur gauche de la boîte.</span><span class="sxs-lookup"><span data-stu-id="e1de0-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="e1de0-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e1de0-114">**ulFlags**</span></span>
  
> <span data-ttu-id="e1de0-115">Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="e1de0-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="e1de0-116">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e1de0-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="e1de0-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1de0-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e1de0-118">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1de0-118">The label is in Unicode format.</span></span> <span data-ttu-id="e1de0-119">Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e1de0-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1de0-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1de0-120">Remarks</span></span>

<span data-ttu-id="e1de0-121">Une structure **DTBLGROUPBOX** décrit un contrôle de zone de groupe qui permet d’associer visuellement des autres contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e1de0-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="e1de0-122">Mise en surbrillance repose entourant les autres contrôles à une zone.</span><span class="sxs-lookup"><span data-stu-id="e1de0-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="e1de0-123">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e1de0-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e1de0-124">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e1de0-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1de0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1de0-125">See also</span></span>



[<span data-ttu-id="e1de0-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e1de0-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e1de0-127">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e1de0-127">MAPI Structures</span></span>](mapi-structures.md)

