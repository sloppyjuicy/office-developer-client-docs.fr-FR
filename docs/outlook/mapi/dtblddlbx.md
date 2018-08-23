---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3307bb252ca4436999a541f85657fed9878c798a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579395"
---
# <a name="dtblddlbx"></a><span data-ttu-id="e3723-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="e3723-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="e3723-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3723-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3723-105">Décrit un contrôle de liste déroulante qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3723-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3723-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e3723-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3723-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3723-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="e3723-108">Members</span><span class="sxs-lookup"><span data-stu-id="e3723-108">Members</span></span>

 <span data-ttu-id="e3723-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e3723-109">**ulFlags**</span></span>
  
> <span data-ttu-id="e3723-110">Réservé, doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e3723-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="e3723-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="e3723-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="e3723-112">Balise de propriété pour une propriété de type PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e3723-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="e3723-113">Cette propriété est une des colonnes de la table identifiée par le membre **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="e3723-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="e3723-114">Les valeurs de cette propriété sont affichent dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e3723-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="e3723-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="e3723-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="e3723-116">Balise de propriété pour une propriété d’un type quelconque.</span><span class="sxs-lookup"><span data-stu-id="e3723-116">Property tag for a property of any type.</span></span> <span data-ttu-id="e3723-117">Cette propriété est une des colonnes de la table identifiée par le membre **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="e3723-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="e3723-118">Lorsque l’utilisateur de la liste sélectionne une valeur de propriété pour le membre **ulPRDisplayProperty** à partir des lignes de la table identifiée par le membre **ulPRTableName** , le membre **ulPRSetProperty** correspondant est défini.</span><span class="sxs-lookup"><span data-stu-id="e3723-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="e3723-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="e3723-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="e3723-120">Balise de propriété pour une propriété de tableau de type PT_OBJECT qui peuvent être ouverts à l’aide d’un **OpenProperty** appeler.</span><span class="sxs-lookup"><span data-stu-id="e3723-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="e3723-121">Le tableau doit avoir deux colonnes : **ulPRDisplayProperty** et **ulPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="e3723-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="e3723-122">Les lignes du tableau doivent correspondre aux éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="e3723-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3723-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3723-123">Remarks</span></span>

<span data-ttu-id="e3723-124">Une structure **DTBLDDLBX** décrit un contrôle de liste déroulante qui s’affiche sous la forme d’un seul élément jusqu'à ce que l’utilisateur choisit pour le développer.</span><span class="sxs-lookup"><span data-stu-id="e3723-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="e3723-125">Les trois propriétés identifiées par les balises de propriété fonctionnent ensemble pour afficher les informations dans la liste et définir une propriété connexe.</span><span class="sxs-lookup"><span data-stu-id="e3723-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="e3723-126">Le membre **ulPRTableName** est un objet table qui est accessible via un appel à [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="e3723-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="e3723-127">La table contient deux colonnes : une colonne pour la propriété identifiée par le membre **ulPRDisplayProperty** et l’autre pour la propriété identifiée par le membre **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="e3723-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="e3723-128">La propriété **ulPRDisplayProperty** gère l’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="e3723-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="e3723-129">Lorsqu’un utilisateur sélectionne une des valeurs de l’affichage, [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir la propriété correspondante tels qu’identifiés par le membre **ulPRSetProperty** appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="e3723-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e3723-130">Cela signifie que la propriété dans la même ligne que la propriété affichage sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e3723-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="e3723-131">Le membre **ulPRSetProperty** ne peut pas être défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e3723-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="e3723-132">Une valeur initiale s’affiche dans la liste si MAPI a récupéré de la propriété représentée par le membre **ulPRSetProperty** via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) et trouve une ligne dans la table avec la valeur du membre **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="e3723-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e3723-133">La valeur affichée initiale est le contenu de la colonne **ulPRDisplayProperty** à partir de la ligne qui correspond à la propriété dans le membre **ulPRDisplayProperty** de la structure.</span><span class="sxs-lookup"><span data-stu-id="e3723-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="e3723-134">La valeur renvoyée par **GetProps** pour la propriété identifiée par le membre **ulPRDisplayProperty** devient la valeur initiale qui s’affiche lors du premier affichage de la liste.</span><span class="sxs-lookup"><span data-stu-id="e3723-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="e3723-135">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e3723-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e3723-136">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e3723-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="e3723-137">Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e3723-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3723-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3723-138">See also</span></span>



[<span data-ttu-id="e3723-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e3723-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="e3723-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e3723-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="e3723-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e3723-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="e3723-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e3723-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="e3723-143">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e3723-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="e3723-144">Implémentation d’un tableau d’affichage</span><span class="sxs-lookup"><span data-stu-id="e3723-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="e3723-145">Tableaux d’affichage</span><span class="sxs-lookup"><span data-stu-id="e3723-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="e3723-146">Vue d’ensemble des types de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="e3723-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

