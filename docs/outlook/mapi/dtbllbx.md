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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438567"
---
# <a name="dtbllbx"></a><span data-ttu-id="df138-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="df138-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="df138-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df138-105">Décrit une liste qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="df138-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df138-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="df138-106">Header file:</span></span>  <br/> |<span data-ttu-id="df138-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df138-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="df138-108">Membres</span><span class="sxs-lookup"><span data-stu-id="df138-108">Members</span></span>

 <span data-ttu-id="df138-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="df138-109">**ulFlags**</span></span>
  
> <span data-ttu-id="df138-110">Masque de bits d’indicateurs utilisé pour éliminer une barre de défilement horizontale ou verticale de la liste.</span><span class="sxs-lookup"><span data-stu-id="df138-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="df138-111">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="df138-111">The following flags can be set:</span></span>
    
<span data-ttu-id="df138-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="df138-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="df138-113">Aucune barre de défilement horizontale ne doit être affichée avec la liste.</span><span class="sxs-lookup"><span data-stu-id="df138-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="df138-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="df138-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="df138-115">Aucune barre de défilement verticale ne doit être affichée avec la liste.</span><span class="sxs-lookup"><span data-stu-id="df138-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="df138-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="df138-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="df138-117">Balise de propriété pour une propriété de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="df138-117">Property tag for a property of any type.</span></span> <span data-ttu-id="df138-118">Cette propriété est l’une des colonnes du tableau identifiées par le **membre ulPRTableTable.**</span><span class="sxs-lookup"><span data-stu-id="df138-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="df138-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="df138-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="df138-120">Balise de propriété pour une propriété de table de type PT_OBJECT qui peut être ouvert à l’aide d’un **appel OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="df138-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="df138-121">Le nombre de colonnes que le tableau doit avoir varie selon que la liste est une liste de sélection unique ou multiple.</span><span class="sxs-lookup"><span data-stu-id="df138-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="df138-122">Si le **membre ulPRSetProperty** est PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)), la liste autorise la sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="df138-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df138-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="df138-123">Remarks</span></span>

<span data-ttu-id="df138-124">Une structure **DTBLLBX** décrit une liste qui est utilisée pour afficher plusieurs éléments et permet à un utilisateur de sélectionner un ou plusieurs des éléments.</span><span class="sxs-lookup"><span data-stu-id="df138-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="df138-125">Le **membre ulPRSetProperty** et le membre **ulPRTableName** fonctionnent ensemble . lorsqu’une valeur est choisie dans le tableau, elle est écrite dans **ulPRSetProperty** lorsque la boîte de dialogue est rejetée.</span><span class="sxs-lookup"><span data-stu-id="df138-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="df138-126">La valeur des indicateurs indique si une barre de défilement horizontale ou verticale doit être affichée avec la liste.</span><span class="sxs-lookup"><span data-stu-id="df138-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="df138-127">Par défaut, des types de barres de défilement doivent apparaître si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="df138-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="df138-128">Les fournisseurs de services peuvent définir des MAPI_NO_HBAR pour supprimer une barre de défilement horizontale et MAPI_NO_VBAR supprimer une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="df138-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="df138-129">Les deux membres de balise de propriété fonctionnent ensemble pour afficher les valeurs dans la liste et définir les propriétés correspondantes lorsqu’un élément de la liste est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="df138-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="df138-130">Lorsque MAPI affiche la liste pour la première fois, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** pour récupérer la table identifiée dans le membre **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="df138-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="df138-131">Le nombre de colonnes dans le tableau dépend de la valeur du **membre ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="df138-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="df138-132">Si **ulPRSetProperty** est définie sur **PR_NULL**, la liste est une liste de sélections multiples basée sur un objet qui contient des destinataires, tels qu’un conteneur de carnet d’adresses, une table des destinataires pour un message ou une table de contenu de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="df138-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="df138-133">Un tableau pour une liste de sélections multiples doit inclure les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="df138-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="df138-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df138-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="df138-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df138-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="df138-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df138-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="df138-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) et un maximum de cinq autres propriétés de chaîne à valeurs multiples peuvent également être affichés avec les trois colonnes requises.</span><span class="sxs-lookup"><span data-stu-id="df138-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="df138-138">Si le **membre ulPRSetProperty** n’est pas PR_NULL **,** la liste est une liste de sélection unique.</span><span class="sxs-lookup"><span data-stu-id="df138-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="df138-139">La valeur initiale de **ulPRSetProperty** détermine la première ligne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="df138-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="df138-140">Lorsqu’un utilisateur sélectionne l’une des lignes, le membre **ulPRSetProperty** est définie sur la valeur sélectionnée et cette valeur est écrite dans l’implémentation de l’interface de propriétés avec un appel à [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="df138-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="df138-141">Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="df138-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="df138-142">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="df138-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df138-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df138-143">See also</span></span>



[<span data-ttu-id="df138-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="df138-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="df138-145">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="df138-145">MAPI Structures</span></span>](mapi-structures.md)

