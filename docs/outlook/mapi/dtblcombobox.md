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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287467"
---
# <a name="dtblcombobox"></a><span data-ttu-id="ebd06-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="ebd06-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="ebd06-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebd06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebd06-105">Décrit un contrôle de zone de liste déroulante qui sera utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="ebd06-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebd06-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ebd06-106">Header file:</span></span>  <br/> |<span data-ttu-id="ebd06-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ebd06-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ebd06-108">Macro connexe:</span><span class="sxs-lookup"><span data-stu-id="ebd06-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ebd06-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="ebd06-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="ebd06-110">Members</span><span class="sxs-lookup"><span data-stu-id="ebd06-110">Members</span></span>

 <span data-ttu-id="ebd06-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="ebd06-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="ebd06-112">Offset entre le début de la structure **DTBLCOMBOBOX** et un filtre de chaîne de caractères qui décrit les restrictions, le cas échéant, des caractères pouvant être entrés dans le contrôle d'édition de la zone de liste modifiable.</span><span class="sxs-lookup"><span data-stu-id="ebd06-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="ebd06-113">Le filtre n'est pas interprété comme une expression régulière et le même filtre est appliqué à tous les caractères entrés.</span><span class="sxs-lookup"><span data-stu-id="ebd06-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="ebd06-114">Le format du filtre est le suivant:</span><span class="sxs-lookup"><span data-stu-id="ebd06-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="ebd06-115">**Caractère**</span><span class="sxs-lookup"><span data-stu-id="ebd06-115">**Character**</span></span>|<span data-ttu-id="ebd06-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="ebd06-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="ebd06-117">N'importe quel caractère est autorisé (par `"*"`exemple,).</span><span class="sxs-lookup"><span data-stu-id="ebd06-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="ebd06-118">Définit un jeu de caractères (par exemple, `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="ebd06-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="ebd06-119">Indique une plage de caractères (par exemple, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="ebd06-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="ebd06-120">Indique que ces caractères ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="ebd06-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="ebd06-121">(par exemple, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="ebd06-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="ebd06-122">Utilisé pour citer tous les symboles précédents (par exemple, `"[\-\\\[\]]"` les caractères «, \, » et «») sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="ebd06-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="ebd06-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ebd06-123">**ulFlags**</span></span>
  
> <span data-ttu-id="ebd06-124">Masque de des indicateurs utilisé pour désigner le format du filtre de chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="ebd06-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="ebd06-125">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="ebd06-125">The following flag can be set:</span></span>
    
<span data-ttu-id="ebd06-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ebd06-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ebd06-127">Le filtre est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ebd06-127">The filter is in Unicode format.</span></span> <span data-ttu-id="ebd06-128">Si l'indicateur MAPI_UNICODE n'est pas défini, le filtre est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ebd06-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="ebd06-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="ebd06-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="ebd06-130">Nombre maximal de caractères pouvant être entrés dans la zone de texte de la zone de liste modifiable.</span><span class="sxs-lookup"><span data-stu-id="ebd06-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="ebd06-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="ebd06-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="ebd06-132">Balise de propriété pour une propriété de type PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="ebd06-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="ebd06-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="ebd06-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="ebd06-134">Balise de propriété pour une propriété de type PT_OBJECT sur laquelle une interface **IMAPITable** peut être ouverte à l'aide d'un appel **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="ebd06-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="ebd06-135">La table doit contenir une colonne avec une propriété qui est du même type que la propriété identifiée par le membre **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="ebd06-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="ebd06-136">Les lignes du tableau sont utilisées pour remplir la liste.</span><span class="sxs-lookup"><span data-stu-id="ebd06-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ebd06-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebd06-137">Remarks</span></span>

<span data-ttu-id="ebd06-138">Une structure **DTBLCOMBOBOX** décrit un contrôle de zone de liste déroulante qui se compose d'une liste et d'un champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="ebd06-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="ebd06-139">La liste présente les informations qu'un utilisateur peut sélectionner et le champ de sélection affiche la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ebd06-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="ebd06-140">Le champ de sélection est un contrôle d'édition qui peut également être utilisé pour entrer du texte qui n'est pas déjà dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ebd06-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="ebd06-141">Les deux membres de la balise de propriété s'emploient ensemble pour coordonner l'affichage de liste avec le contrôle d'édition.</span><span class="sxs-lookup"><span data-stu-id="ebd06-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="ebd06-142">Lorsque MAPI affiche d'abord la zone de liste déroulante, il appelle la méthode **OpenProperty** de l'implémentation **IMAPIProp** associée à la table d'affichage pour récupérer la table représentée par le membre **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="ebd06-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="ebd06-143">Cette table comporte une colonne une colonne qui contient les valeurs de la propriété représentée par le membre **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="ebd06-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="ebd06-144">Par conséquent, cette colonne doit être du même type que la propriété **ulPRPropertyName** et les deux colonnes doivent être des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="ebd06-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="ebd06-145">Les valeurs de la colonne sont affichées dans la section de liste de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ebd06-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="ebd06-146">Par conséquent, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) n'est pas une balise de propriété valide pour **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="ebd06-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="ebd06-147">Lorsqu'un utilisateur sélectionne une des lignes ou entre de nouvelles données dans la zone de texte, la propriété **ulPRPropertyName** est définie sur la valeur sélectionnée ou entrée.</span><span class="sxs-lookup"><span data-stu-id="ebd06-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="ebd06-148">Pour afficher une valeur initiale pour le contrôle d'édition, MAPI appelle [IMAPIProp:: GetProps](imapiprop-getprops.md) pour récupérer les valeurs de propriété de la table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="ebd06-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="ebd06-149">Si l'une des propriétés récupérées correspond à la propriété représentée par le membre **ulPRPropertyName** , sa valeur devient la valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="ebd06-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="ebd06-150">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ebd06-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ebd06-151">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="ebd06-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebd06-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd06-152">See also</span></span>



[<span data-ttu-id="ebd06-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ebd06-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="ebd06-154">Propriété canonique PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="ebd06-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="ebd06-155">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd06-155">MAPI Structures</span></span>](mapi-structures.md)

