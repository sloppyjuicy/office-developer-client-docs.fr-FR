---
title: Propriété canonique PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785884"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="fa1a7-103">Propriété canonique PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="fa1a7-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="fa1a7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa1a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa1a7-105">Contient un masque de bits d’indicateurs régissant le comportement d’un contrôle utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa1a7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fa1a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa1a7-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="fa1a7-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="fa1a7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fa1a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa1a7-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="fa1a7-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="fa1a7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fa1a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa1a7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fa1a7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fa1a7-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="fa1a7-112">Area:</span></span>  <br/> |<span data-ttu-id="fa1a7-113">Afficher une table MAPI</span><span class="sxs-lookup"><span data-stu-id="fa1a7-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa1a7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa1a7-114">Remarks</span></span>

<span data-ttu-id="fa1a7-115">Un ou plusieurs des indicateurs suivants peuvent être définie pour cette propriété :</span><span class="sxs-lookup"><span data-stu-id="fa1a7-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="fa1a7-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="fa1a7-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="fa1a7-117">Le contrôle peut contenir des caractères de définir de caractères codés sur deux octets (DBCS) qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="fa1a7-118">Cet indicateur est utilisé avec les contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-118">This flag is used with edit controls.</span></span> <span data-ttu-id="fa1a7-119">Il permet de jeux de caractères codés sur plusieurs.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="fa1a7-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="fa1a7-121">Le contrôle peut être modifié ; la valeur associée au contrôle peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="fa1a7-122">Lorsque cet indicateur n’est pas défini, le contrôle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="fa1a7-123">Cette valeur est ignorée sur l’étiquette, zone de groupe, bouton de commande standard, à valeurs multiples de liste déroulante zone de liste et les contrôles de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="fa1a7-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="fa1a7-125">Le contrôle d’édition peut contenir plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="fa1a7-126">Cela signifie qu'un caractère de retour peut être entré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="fa1a7-127">Cet indicateur n’est valide que pour les contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="fa1a7-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="fa1a7-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="fa1a7-129">S’applique aux contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-129">Applies to edit controls.</span></span> <span data-ttu-id="fa1a7-130">Le contrôle d’édition est traité comme un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-130">The edit control is treated like a password.</span></span> <span data-ttu-id="fa1a7-131">La valeur est affichée à l’aide d’astérisques au lieu de la résonance des caractères entrés.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="fa1a7-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="fa1a7-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="fa1a7-133">Si le contrôle autorise les modifications (DT_EDITABLE), il doit avoir une valeur [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="fa1a7-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="fa1a7-135">Active un paramètre exécution d’une valeur ; dès qu’une valeur dans le contrôle change, MAPI appelle la méthode **SetProps** pour la propriété associée à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="fa1a7-136">Lorsque cet indicateur n’est pas défini, les valeurs sont définies lorsque la boîte de dialogue est fermée.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="fa1a7-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="fa1a7-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="fa1a7-138">Lorsqu’une sélection est effectuée dans la zone de liste, la colonne de l’index de cette zone de liste est définie en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="fa1a7-139">Toujours utilisé avec DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="fa1a7-140">Cette propriété est stockée dans le membre ulCtlFlags de structure de [DTCTL](dtctl.md) d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="fa1a7-141">La plupart des indicateurs de contrôle qui s’appliquent à tous les contrôles qui autorisent les entrées utilisateur ; quelques-unes s’appliquent uniquement au contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="fa1a7-142">Les contrôles qui n’autorisent pas l’entrée de l’utilisateur, par exemple un bouton ou une étiquette, la valeur 0 pour les indicateurs de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="fa1a7-143">La plupart des valeurs d’indicateur sont explicites.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="fa1a7-144">Par exemple, lorsque DT_REQUIRED est définie pour un contrôle, il doit contenir une valeur avant de la boîte de dialogue est autorisée à être fermée.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="fa1a7-145">Le fournisseur de services peut fournir une valeur via son implémentation **IMAPIProp** ou l’utilisateur peut entrer un.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="fa1a7-146">DT_EDITABLE indique que la valeur du contrôle peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="fa1a7-147">DT_MULTILINE permet à la valeur d’un contrôle d’édition de couvrir plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="fa1a7-148">Certains indicateurs de contrôle ne sont pas évidentes dans leur signification.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="fa1a7-149">Lorsqu’un contrôle définit l’indicateur DT_SET_IMMEDIATE, les modifications à prendre de sa valeur affectent dès que l’utilisateur déplace vers un nouveau contrôle.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="fa1a7-150">MAPI permet à un seul appel à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’interface propriété pour la propriété du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="fa1a7-151">Cela diffère le comportement par défaut, qui consiste à différer ayant des modifications apportées aux valeurs de contrôle prendront effet qu’après que l’utilisateur sélectionne le bouton **OK** ou ferme la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="fa1a7-152">L’indicateur DT_SET_IMMEDIATE est souvent utilisée en combinaison avec afficher les notifications de table.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="fa1a7-153">Le tableau suivant répertorie les types de contrôles et toutes les valeurs d’indicateur qui peuvent être définies pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="fa1a7-154">**Contrôle**</span><span class="sxs-lookup"><span data-stu-id="fa1a7-154">**Control**</span></span>|<span data-ttu-id="fa1a7-155">**Valeurs valides pour cette propriété**</span><span class="sxs-lookup"><span data-stu-id="fa1a7-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa1a7-156">Bouton</span><span class="sxs-lookup"><span data-stu-id="fa1a7-156">Button</span></span>  <br/> |<span data-ttu-id="fa1a7-157">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-158">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="fa1a7-158">Check box</span></span>  <br/> |<span data-ttu-id="fa1a7-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="fa1a7-160">Zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="fa1a7-160">Combo box</span></span>  <br/> |<span data-ttu-id="fa1a7-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="fa1a7-162">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="fa1a7-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="fa1a7-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="fa1a7-164">Modifier</span><span class="sxs-lookup"><span data-stu-id="fa1a7-164">Edit</span></span>  <br/> |<span data-ttu-id="fa1a7-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="fa1a7-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="fa1a7-166">Zone de groupe</span><span class="sxs-lookup"><span data-stu-id="fa1a7-166">Group box</span></span>  <br/> |<span data-ttu-id="fa1a7-167">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-168">Étiquette</span><span class="sxs-lookup"><span data-stu-id="fa1a7-168">Label</span></span>  <br/> |<span data-ttu-id="fa1a7-169">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-170">Zone de liste</span><span class="sxs-lookup"><span data-stu-id="fa1a7-170">List box</span></span>  <br/> |<span data-ttu-id="fa1a7-171">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-172">Zone de liste déroulante à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="fa1a7-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="fa1a7-173">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-174">Zone de liste à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="fa1a7-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="fa1a7-175">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-176">Page à onglets</span><span class="sxs-lookup"><span data-stu-id="fa1a7-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="fa1a7-177">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="fa1a7-178">Case d’option</span><span class="sxs-lookup"><span data-stu-id="fa1a7-178">Radio button</span></span>  <br/> |<span data-ttu-id="fa1a7-179">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="fa1a7-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fa1a7-180">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fa1a7-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fa1a7-181">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fa1a7-181">Header files</span></span>

<span data-ttu-id="fa1a7-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa1a7-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa1a7-183">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa1a7-184">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="fa1a7-184">Mapitags.h</span></span>
  
> <span data-ttu-id="fa1a7-185">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="fa1a7-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa1a7-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa1a7-186">See also</span></span>



[<span data-ttu-id="fa1a7-187">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fa1a7-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa1a7-188">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fa1a7-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa1a7-189">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fa1a7-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa1a7-190">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="fa1a7-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

