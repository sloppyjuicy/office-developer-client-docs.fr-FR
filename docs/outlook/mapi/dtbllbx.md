---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569763"
---
# <a name="dtbllbx"></a><span data-ttu-id="9927a-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="9927a-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="9927a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9927a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9927a-105">Décrit une liste qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9927a-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9927a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9927a-106">Header file:</span></span>  <br/> |<span data-ttu-id="9927a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9927a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="9927a-108">Members</span><span class="sxs-lookup"><span data-stu-id="9927a-108">Members</span></span>

 <span data-ttu-id="9927a-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9927a-109">**ulFlags**</span></span>
  
> <span data-ttu-id="9927a-110">Masque de bits d’indicateurs utilisés pour supprimer une barre de défilement horizontal ou vertical dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9927a-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="9927a-111">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="9927a-111">The following flags can be set:</span></span>
    
<span data-ttu-id="9927a-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="9927a-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="9927a-113">Aucune barre de défilement horizontale ne doit être affichée dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9927a-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="9927a-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="9927a-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="9927a-115">Aucune barre de défilement verticale ne doit être affichée dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9927a-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="9927a-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="9927a-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="9927a-117">Balise de propriété pour une propriété d’un type quelconque.</span><span class="sxs-lookup"><span data-stu-id="9927a-117">Property tag for a property of any type.</span></span> <span data-ttu-id="9927a-118">Cette propriété est une des colonnes de la table identifiée par le membre **ulPRTableTable** .</span><span class="sxs-lookup"><span data-stu-id="9927a-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="9927a-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="9927a-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="9927a-120">Balise de propriété pour une propriété de tableau de type PT_OBJECT qui peuvent être ouverts à l’aide d’un **OpenProperty** appeler.</span><span class="sxs-lookup"><span data-stu-id="9927a-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="9927a-121">Le nombre de colonnes pour la table varie selon que la liste est une liste à sélection unique ou multiple.</span><span class="sxs-lookup"><span data-stu-id="9927a-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="9927a-122">Si le membre **ulPRSetProperty** est défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la liste permet à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="9927a-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9927a-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="9927a-123">Remarks</span></span>

<span data-ttu-id="9927a-124">Une structure **DTBLLBX** décrit un contrôle qui est utilisé pour afficher plusieurs éléments et permettent à un utilisateur de sélectionner une ou plusieurs des éléments de liste.</span><span class="sxs-lookup"><span data-stu-id="9927a-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="9927a-125">Le membre **ulPRSetProperty** et **ulPRTableName** membre collaborent ; Lorsque vous sélectionnez une valeur de la table, il est réécrit dans **ulPRSetProperty** lorsque la boîte de dialogue est fermée.</span><span class="sxs-lookup"><span data-stu-id="9927a-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="9927a-126">La valeur flags indique si une barre de défilement horizontale ou verticale doit être affichée avec la liste.</span><span class="sxs-lookup"><span data-stu-id="9927a-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="9927a-127">La valeur par défaut est d’avoir des types de défilement barres s’affichent si cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9927a-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="9927a-128">Fournisseurs de services peuvent définir MAPI_NO_HBAR pour supprimer une barre de défilement horizontale et MAPI_NO_VBAR pour supprimer une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="9927a-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="9927a-129">Les membres de balise de deux propriété travaillent ensemble pour afficher les valeurs dans la liste et définir les propriétés correspondantes lorsqu’un élément dans la liste est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9927a-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="9927a-130">Lorsque tout d’abord, MAPI affiche la liste, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** pour récupérer la table identifiée dans le membre **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="9927a-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="9927a-131">Le nombre de colonnes dans le tableau dépend de la valeur du membre **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="9927a-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="9927a-132">Si **ulPRSetProperty** est défini sur **PR_NULL**, la liste est une liste de sélection de plusieurs basée sur un objet qui contient les destinataires, comme un conteneur de carnet d’adresses, une table de destinataires pour un message ou un tableau de contenu de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="9927a-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="9927a-133">Un objet table pour une liste de sélection multiple doit inclure les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9927a-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="9927a-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9927a-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="9927a-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9927a-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="9927a-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9927a-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="9927a-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) et un maximum de cinq autres propriétés de type chaîne à valeurs multiples peut également être affiché avec les trois colonnes requises.</span><span class="sxs-lookup"><span data-stu-id="9927a-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="9927a-138">Si le membre **ulPRSetProperty** n’est pas défini sur **PR_NULL**, la liste est une liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="9927a-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="9927a-139">La valeur initiale de **ulPRSetProperty** détermine la première ligne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9927a-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="9927a-140">Lorsqu’un utilisateur sélectionne une des lignes, le membre **ulPRSetProperty** est défini à la valeur sélectionnée et cette valeur est réécrit dans l’implémentation d’interface de propriété avec un appel à [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="9927a-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="9927a-141">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9927a-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="9927a-142">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9927a-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9927a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9927a-143">See also</span></span>



[<span data-ttu-id="9927a-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="9927a-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="9927a-145">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9927a-145">MAPI Structures</span></span>](mapi-structures.md)

