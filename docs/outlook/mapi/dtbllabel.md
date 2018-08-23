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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 09f0d7988f85a6d6018c45cb64245ab331cda052
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582811"
---
# <a name="dtbllabel"></a><span data-ttu-id="49b33-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="49b33-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="49b33-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49b33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49b33-105">Décrit une étiquette qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="49b33-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49b33-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="49b33-106">Header file:</span></span>  <br/> |<span data-ttu-id="49b33-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49b33-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="49b33-108">Macro connexe</span><span class="sxs-lookup"><span data-stu-id="49b33-108">Related macro</span></span>  <br/> |[<span data-ttu-id="49b33-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="49b33-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="49b33-110">Members</span><span class="sxs-lookup"><span data-stu-id="49b33-110">Members</span></span>

 <span data-ttu-id="49b33-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="49b33-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="49b33-112">Position dans la mémoire de l’étiquette de chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="49b33-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="49b33-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="49b33-113">**ulFlags**</span></span>
  
> <span data-ttu-id="49b33-114">Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="49b33-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="49b33-115">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="49b33-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="49b33-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49b33-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="49b33-117">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="49b33-117">The label is in Unicode format.</span></span> <span data-ttu-id="49b33-118">Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="49b33-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49b33-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="49b33-119">Remarks</span></span>

<span data-ttu-id="49b33-120">Une structure **DTBLLABEL** décrit un texte de contrôle d’étiquette qui s’affiche avec un autre type de contrôle à ajouter la signification de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="49b33-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="49b33-121">Par exemple, la plupart des contrôles d’édition sont positionnés en regard des étiquettes pour informer l’utilisateur à entrer le type d’informations.</span><span class="sxs-lookup"><span data-stu-id="49b33-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="49b33-122">Certains contrôles, tels que les zones de groupe et de cases d’option, maintenez la touche leurs propres étiquettes.</span><span class="sxs-lookup"><span data-stu-id="49b33-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="49b33-123">L’étiquette peut inclure un raccourci Windows, identifiée comme le caractère qui suit le signe (&amp;).</span><span class="sxs-lookup"><span data-stu-id="49b33-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="49b33-124">Appuyer sur la touche d’accès rapide place le focus dans la première nonlabel, contrôle libellés suivant cette étiquette dans le tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="49b33-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="49b33-125">Il n’existe aucune prise en charge pour les étiquettes multilignes.</span><span class="sxs-lookup"><span data-stu-id="49b33-125">There is no support for multiline labels.</span></span> <span data-ttu-id="49b33-126">Afficher plusieurs lignes nécessite plusieurs étiquettes.</span><span class="sxs-lookup"><span data-stu-id="49b33-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="49b33-127">Il n’est pas possible d’utiliser une étiquette comme un contrôle d’édition en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="49b33-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="49b33-128">La différence est qu’un contrôle d’édition peut être sélectionné et copié qu’une étiquette ne peut pas.</span><span class="sxs-lookup"><span data-stu-id="49b33-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="49b33-129">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="49b33-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="49b33-130">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="49b33-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49b33-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49b33-131">See also</span></span>



[<span data-ttu-id="49b33-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="49b33-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="49b33-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="49b33-133">MAPI Structures</span></span>](mapi-structures.md)

