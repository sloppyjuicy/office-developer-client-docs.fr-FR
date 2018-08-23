---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eefd0c62314a35c4c6c956b8d4a4d92d5746d1c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590462"
---
# <a name="dtbledit"></a><span data-ttu-id="09425-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="09425-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="09425-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09425-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09425-105">Décrit un contrôle d’édition qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="09425-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09425-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="09425-106">Header file:</span></span>  <br/> |<span data-ttu-id="09425-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09425-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="09425-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="09425-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="09425-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="09425-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="09425-110">Members</span><span class="sxs-lookup"><span data-stu-id="09425-110">Members</span></span>

 <span data-ttu-id="09425-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="09425-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="09425-112">Décalage à partir du début de la structure **DTBLEDIT** pour un filtre de chaîne de caractères qui décrit les restrictions, le cas échéant, pour les caractères qui peuvent être saisis dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="09425-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="09425-113">Le filtre n’est pas interprété comme une expression régulière et le même filtre est appliqué à tous les caractères entrés.</span><span class="sxs-lookup"><span data-stu-id="09425-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="09425-114">Le format du filtre est comme suit :</span><span class="sxs-lookup"><span data-stu-id="09425-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="09425-115">**Caractère**</span><span class="sxs-lookup"><span data-stu-id="09425-115">**Character**</span></span>|<span data-ttu-id="09425-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="09425-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="09425-117">N’importe quel caractère est autorisé (par exemple, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="09425-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="09425-118">Définit un jeu de caractères (par exemple, `"[0123456789]".`)</span><span class="sxs-lookup"><span data-stu-id="09425-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="09425-119">Indique une plage de caractères (par exemple, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="09425-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="09425-120">Indique que ces caractères ne sont pas autorisés (par exemple, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="09425-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="09425-121">Utilisé pour les symboles précédentes quote (par exemple, `"[\-\\\[\]]"` signifie-, \, [, et] caractères sont autorisés).</span><span class="sxs-lookup"><span data-stu-id="09425-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="09425-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="09425-122">**ulFlags**</span></span>
  
> <span data-ttu-id="09425-123">Masque de bits d’indicateurs utilisés pour désigner le format du filtre de caractères.</span><span class="sxs-lookup"><span data-stu-id="09425-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="09425-124">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="09425-124">The following flag can be set:</span></span>
    
<span data-ttu-id="09425-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09425-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="09425-126">Le filtre est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="09425-126">The filter is in Unicode format.</span></span> <span data-ttu-id="09425-127">Si l’indicateur MAPI_UNICODE n’est pas définie, le filtre est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="09425-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="09425-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="09425-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="09425-129">Nombre maximal de caractères que l’utilisateur peut taper dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="09425-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="09425-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="09425-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="09425-131">Balise de propriété pour une propriété de type PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="09425-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="09425-132">Le membre **ulPropTag** identifie la propriété de type chaîne dont les données sont affichées et modifiées dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="09425-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09425-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="09425-133">Remarks</span></span>

<span data-ttu-id="09425-134">Une structure **DTBLEDIT** décrit un contrôle d’édition à une zone de la boîte de dialogue qui contient des informations alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="09425-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="09425-135">Presque toutes les boîtes de dialogue ont modifier au moins un contrôle.</span><span class="sxs-lookup"><span data-stu-id="09425-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="09425-136">Les contrôles d’édition peuvent être modifiable par un utilisateur ou en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09425-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="09425-137">Les contrôles d’édition peuvent également être la seule ligne ou plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="09425-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="09425-138">Contrôles d’édition multilignes ont généralement une barre de défilement associée.</span><span class="sxs-lookup"><span data-stu-id="09425-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="09425-139">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="09425-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="09425-140">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="09425-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09425-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09425-141">See also</span></span>



[<span data-ttu-id="09425-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="09425-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="09425-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="09425-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="09425-144">Propriété canonique PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="09425-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="09425-145">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="09425-145">MAPI Structures</span></span>](mapi-structures.md)

