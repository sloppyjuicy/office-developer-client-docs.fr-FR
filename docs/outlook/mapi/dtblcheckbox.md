---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436831"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="55e9b-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="55e9b-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="55e9b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55e9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55e9b-105">Contient des informations sur une case à cocher qui sera utilisée dans une boîte de dialogue construite à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="55e9b-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55e9b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="55e9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="55e9b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="55e9b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="55e9b-108">Macro connexe:</span><span class="sxs-lookup"><span data-stu-id="55e9b-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="55e9b-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="55e9b-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="55e9b-110">Members</span><span class="sxs-lookup"><span data-stu-id="55e9b-110">Members</span></span>

 <span data-ttu-id="55e9b-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="55e9b-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="55e9b-112">Position en mémoire de la chaîne de caractères qui s'affiche avec la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="55e9b-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="55e9b-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="55e9b-113">**ulFlags**</span></span>
  
> <span data-ttu-id="55e9b-114">Masque de des indicateurs utilisé pour désigner le format de l'étiquette de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="55e9b-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="55e9b-115">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="55e9b-115">The following flag can be set:</span></span>
    
<span data-ttu-id="55e9b-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="55e9b-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="55e9b-117">L'étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="55e9b-117">The label is in Unicode format.</span></span> <span data-ttu-id="55e9b-118">Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="55e9b-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="55e9b-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="55e9b-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="55e9b-120">Balise de propriété pour une propriété de type PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="55e9b-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="55e9b-121">La valeur de cette propriété est affectée par l'état de la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="55e9b-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55e9b-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="55e9b-122">Remarks</span></span>

<span data-ttu-id="55e9b-123">Une structure **DTBLCHECKBOX** décrit une case à cocher qui reflète l'un des deux États suivants: activé (case cochée) ou désactivé (zone vide).</span><span class="sxs-lookup"><span data-stu-id="55e9b-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="55e9b-124">Le membre **ulPRPropertyName** décrit une propriété booléenne dont la valeur est manipulée en modifiant l'état de la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="55e9b-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="55e9b-125">Lorsque la case à cocher est affichée pour la première fois, MAPI appelle la méthode **GetProps** de l'implémentation **IMAPIProp** associée à la table d'affichage pour récupérer un jeu de propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="55e9b-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="55e9b-126">Si l'une des propriétés est mappée à la balise de propriété dans la structure **DTBLCHECKBOX** , la valeur de cette propriété est affichée en tant que valeur initiale de la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="55e9b-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="55e9b-127">Les contrôles de case à coCher peuvent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="55e9b-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="55e9b-128">Cela permet à un utilisateur de modifier son état.</span><span class="sxs-lookup"><span data-stu-id="55e9b-128">This allows a user to change their states.</span></span> <span data-ttu-id="55e9b-129">Les cases à cocher modifiables définissent l'indicateur DT_EDITABLE dans le membre **ulCtlFlags** de leur structure [DTCTL](dtctl.md) et dans leur propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="55e9b-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="55e9b-130">Lorsqu'une case à cocher modifie son état, MAPI appelle [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir la propriété identifiée dans le membre de la balise de propriété de la structure **DTBLCHECKBOX** sur le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="55e9b-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="55e9b-131">Par exemple, un fournisseur de carnet d'adresses peut inclure un contrôle de case à cocher modifiable dans sa boîte de dialogue de configuration pour ajuster le paramètre de la propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) d'un destinataire.</span><span class="sxs-lookup"><span data-stu-id="55e9b-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="55e9b-132">Lorsque l'utilisateur active la case à cocher, MAPI affecte à cette propriété la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="55e9b-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="55e9b-133">Lorsque la case à cocher est désactivée, la propriété est définie sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="55e9b-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="55e9b-134">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="55e9b-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="55e9b-135">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="55e9b-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="55e9b-136">Pour plus d'informations sur les types de propriétés, voir [MAPI Property type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="55e9b-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55e9b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55e9b-137">See also</span></span>



[<span data-ttu-id="55e9b-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="55e9b-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="55e9b-139">Propriété canonique PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="55e9b-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="55e9b-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="55e9b-140">MAPI Structures</span></span>](mapi-structures.md)

