---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410685"
---
# <a name="dtbllabel"></a><span data-ttu-id="a547d-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="a547d-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="a547d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a547d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a547d-105">Décrit une étiquette qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a547d-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a547d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a547d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a547d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a547d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a547d-108">Macro associée</span><span class="sxs-lookup"><span data-stu-id="a547d-108">Related macro</span></span>  <br/> |[<span data-ttu-id="a547d-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="a547d-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="a547d-110">Members</span><span class="sxs-lookup"><span data-stu-id="a547d-110">Members</span></span>

 <span data-ttu-id="a547d-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="a547d-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="a547d-112">Position en mémoire de l’étiquette de chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="a547d-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="a547d-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a547d-113">**ulFlags**</span></span>
  
> <span data-ttu-id="a547d-114">Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabelName.**</span><span class="sxs-lookup"><span data-stu-id="a547d-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="a547d-115">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="a547d-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="a547d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a547d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a547d-117">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="a547d-117">The label is in Unicode format.</span></span> <span data-ttu-id="a547d-118">Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="a547d-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a547d-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="a547d-119">Remarks</span></span>

<span data-ttu-id="a547d-120">Une structure **DTBLLABEL** décrit un texte de contrôle d’étiquette qui est affiché avec un autre type de contrôle pour ajouter une signification à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="a547d-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="a547d-121">Par exemple, la plupart des contrôles d’édition sont placés à côté des étiquettes pour informer l’utilisateur du type d’informations à entrer.</span><span class="sxs-lookup"><span data-stu-id="a547d-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="a547d-122">Certains contrôles, tels que les cases de groupe et les cases d’radio, tiennent leurs propres étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a547d-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="a547d-123">L’étiquette peut inclure un accélérateur Windows, identifié comme le caractère suivant l’eterrable ( &amp; ).</span><span class="sxs-lookup"><span data-stu-id="a547d-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="a547d-124">Le fait d’appuyer sur la touche d’accélérateur met le focus sur le premier contrôle sans étiquette, nonbutton, qui suit cette étiquette dans le tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a547d-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="a547d-125">Il n’existe aucune prise en charge des étiquettes multilignes.</span><span class="sxs-lookup"><span data-stu-id="a547d-125">There is no support for multiline labels.</span></span> <span data-ttu-id="a547d-126">L’affichage de plusieurs lignes nécessite plusieurs étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a547d-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="a547d-127">Il n’est pas possible d’utiliser une étiquette comme contrôle d’édition en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a547d-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="a547d-128">La différence est qu’un contrôle d’édition peut être sélectionné et copié alors qu’une étiquette ne le peut pas.</span><span class="sxs-lookup"><span data-stu-id="a547d-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="a547d-129">Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="a547d-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="a547d-130">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="a547d-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a547d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a547d-131">See also</span></span>



[<span data-ttu-id="a547d-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="a547d-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="a547d-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="a547d-133">MAPI Structures</span></span>](mapi-structures.md)

