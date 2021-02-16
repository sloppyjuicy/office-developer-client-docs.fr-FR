---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406975"
---
# <a name="dtblcombobox"></a><span data-ttu-id="dee82-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="dee82-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="dee82-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dee82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dee82-105">Décrit un contrôle de zone de liste déroulante qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="dee82-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dee82-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dee82-106">Header file:</span></span>  <br/> |<span data-ttu-id="dee82-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dee82-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dee82-108">Macro associée :</span><span class="sxs-lookup"><span data-stu-id="dee82-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="dee82-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="dee82-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a><span data-ttu-id="dee82-110">Members</span><span class="sxs-lookup"><span data-stu-id="dee82-110">Members</span></span>

 <span data-ttu-id="dee82-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="dee82-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="dee82-112">Décalage entre le début de la structure **DTBLCOMBOBOX** et un filtre de chaîne de caractères qui décrit les restrictions, le casque, et les caractères qui peuvent être entrés dans le contrôle d’édition de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="dee82-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="dee82-113">Le filtre n’est pas interprété comme une expression régulière et le même filtre est appliqué à chaque caractère entré.</span><span class="sxs-lookup"><span data-stu-id="dee82-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="dee82-114">Le format du filtre est le suivant :</span><span class="sxs-lookup"><span data-stu-id="dee82-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="dee82-115">**Caractère**</span><span class="sxs-lookup"><span data-stu-id="dee82-115">**Character**</span></span>|<span data-ttu-id="dee82-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="dee82-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="dee82-117">Tout caractère est autorisé (par exemple,  `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="dee82-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="dee82-118">Définit un ensemble de caractères (par exemple,  `"[0123456789]"` ).</span><span class="sxs-lookup"><span data-stu-id="dee82-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="dee82-119">Indique une plage de caractères (par exemple,  `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="dee82-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="dee82-120">Indique que ces caractères ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="dee82-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="dee82-121">(par exemple,  `"[~0-9]"` ).</span><span class="sxs-lookup"><span data-stu-id="dee82-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="dee82-122">Utilisé pour guillemets l’un des symboles précédents (par exemple, les caractères  `"[\-\\\[\]]"` -, \, [et ] sont autorisés).</span><span class="sxs-lookup"><span data-stu-id="dee82-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="dee82-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="dee82-123">**ulFlags**</span></span>
  
> <span data-ttu-id="dee82-124">Masque de bits d’indicateurs utilisés pour désigner le format du filtre de chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="dee82-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="dee82-125">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="dee82-125">The following flag can be set:</span></span>
    
<span data-ttu-id="dee82-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dee82-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dee82-127">Le filtre est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="dee82-127">The filter is in Unicode format.</span></span> <span data-ttu-id="dee82-128">Si l MAPI_UNICODE n’est pas définie, le filtre est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="dee82-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="dee82-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="dee82-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="dee82-130">Nombre maximal de caractères qui peuvent être entrés dans la zone de texte de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="dee82-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="dee82-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="dee82-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="dee82-132">Balise de propriété pour une propriété de type PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="dee82-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="dee82-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="dee82-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="dee82-134">Balise de propriété pour une propriété de type PT_OBJECT sur laquelle une interface **IMAPITable** peut être ouverte à l’aide d’un **appel OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="dee82-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="dee82-135">La table doit avoir une colonne avec une propriété du même type que la propriété identifiée par le membre **ulPRPropertyName.**</span><span class="sxs-lookup"><span data-stu-id="dee82-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="dee82-136">Les lignes du tableau sont utilisées pour remplir la liste.</span><span class="sxs-lookup"><span data-stu-id="dee82-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dee82-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="dee82-137">Remarks</span></span>

<span data-ttu-id="dee82-138">Une structure **DTBLCOMBOBOX** décrit une zone de liste déroulante composée d’une liste et d’un champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="dee82-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="dee82-139">La liste présente les informations à partir des lesquelles un utilisateur peut sélectionner, et le champ de sélection affiche la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="dee82-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="dee82-140">Le champ de sélection est un contrôle d’édition qui peut également être utilisé pour entrer du texte qui n’est pas déjà dans la liste.</span><span class="sxs-lookup"><span data-stu-id="dee82-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="dee82-141">Les deux membres de balise de propriété fonctionnent ensemble pour coordonner l’affichage de la liste avec le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="dee82-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="dee82-142">Lorsque MAPI affiche la zone de liste déroulante pour la première fois, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** associée à la table d’affichage pour récupérer la table représentée par le membre **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="dee82-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="dee82-143">Cette table contient une colonne contenant les valeurs de la propriété représentée par le membre **ulPRPropertyName.**</span><span class="sxs-lookup"><span data-stu-id="dee82-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="dee82-144">Par conséquent, cette colonne doit être du même type que la propriété **ulPRPropertyName** et les deux colonnes doivent être des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="dee82-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="dee82-145">Les valeurs de la colonne sont affichées dans la section liste de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="dee82-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="dee82-146">Par conséquent, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) n’est pas une balise de propriété valide pour **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="dee82-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="dee82-147">Lorsqu’un utilisateur sélectionne l’une des lignes ou entre de nouvelles données dans la zone de texte, la propriété **ulPRPropertyName** est définie sur la valeur sélectionnée ou entrée.</span><span class="sxs-lookup"><span data-stu-id="dee82-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="dee82-148">Pour afficher une valeur initiale pour le contrôle d’édition, MAPI appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer les valeurs de propriété du tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="dee82-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="dee82-149">Si l’une des propriétés récupérées correspond à la propriété représentée par le membre **ulPRPropertyName,** sa valeur devient la valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="dee82-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="dee82-150">Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="dee82-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="dee82-151">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="dee82-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dee82-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dee82-152">See also</span></span>



[<span data-ttu-id="dee82-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="dee82-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="dee82-154">Propriété canonique PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="dee82-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="dee82-155">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="dee82-155">MAPI Structures</span></span>](mapi-structures.md)

