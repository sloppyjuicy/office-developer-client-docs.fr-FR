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
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331863"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="416f6-103">Propriété canonique PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="416f6-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="416f6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="416f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="416f6-105">Contient un masque de réindicateur des indicateurs régissant le comportement d'un contrôle utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="416f6-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="416f6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="416f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="416f6-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="416f6-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="416f6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="416f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="416f6-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="416f6-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="416f6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="416f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="416f6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="416f6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="416f6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="416f6-112">Area:</span></span>  <br/> |<span data-ttu-id="416f6-113">Table d'affichage MAPI</span><span class="sxs-lookup"><span data-stu-id="416f6-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="416f6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="416f6-114">Remarks</span></span>

<span data-ttu-id="416f6-115">Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété:</span><span class="sxs-lookup"><span data-stu-id="416f6-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="416f6-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="416f6-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="416f6-117">Le contrôle peut contenir des caractères DBCS (Double-Byte Character Set).</span><span class="sxs-lookup"><span data-stu-id="416f6-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="416f6-118">Cet indicateur est utilisé avec les contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="416f6-118">This flag is used with edit controls.</span></span> <span data-ttu-id="416f6-119">Il autorise des jeux de caractères codés sur plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="416f6-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="416f6-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="416f6-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="416f6-121">Le contrôle peut être modifié; la valeur associée au contrôle peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="416f6-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="416f6-122">Lorsque cet indicateur n'est pas défini, le contrôle est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="416f6-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="416f6-123">Cette valeur est ignorée sur l'étiquette, la zone de groupe, le bouton de commande standard, la zone de liste déroulante à valeurs multiples et les contrôles de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="416f6-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="416f6-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="416f6-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="416f6-125">Le contrôle d'édition peut contenir plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="416f6-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="416f6-126">Cela signifie qu'un caractère de retour peut être entré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="416f6-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="416f6-127">Cet indicateur est valide uniquement pour les contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="416f6-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="416f6-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="416f6-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="416f6-129">S'applique aux contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="416f6-129">Applies to edit controls.</span></span> <span data-ttu-id="416f6-130">Le contrôle d'édition est traité comme un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="416f6-130">The edit control is treated like a password.</span></span> <span data-ttu-id="416f6-131">La valeur est affichée à l'aide d'astérisques au lieu de renvoyer les caractères réels entrés.</span><span class="sxs-lookup"><span data-stu-id="416f6-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="416f6-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="416f6-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="416f6-133">Si le contrôle autorise les modifications (DT_EDITABLE), il doit avoir une valeur avant [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="416f6-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="416f6-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="416f6-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="416f6-135">Active le paramétrage immédiat d'une valeur; dès qu'une valeur du contrôle est modifiée, MAPI appelle la méthode **SetProps** pour la propriété associée à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="416f6-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="416f6-136">Lorsque cet indicateur n'est pas défini, les valeurs sont définies lorsque la boîte de dialogue est fermée.</span><span class="sxs-lookup"><span data-stu-id="416f6-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="416f6-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="416f6-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="416f6-138">Lorsqu'une sélection est effectuée dans la zone de liste, la colonne d'index de cette zone de liste est définie en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="416f6-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="416f6-139">Toujours utilisé avec DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="416f6-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="416f6-140">Cette propriété est stockée dans le membre ulCtlFlags de la structure [DTCTL](dtctl.md) d'un contrôle.</span><span class="sxs-lookup"><span data-stu-id="416f6-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="416f6-141">La plupart des indicateurs de contrôle s'appliquent à tous les contrôles qui autorisent l'entrée de l'utilisateur; quelques-unes s'appliquent uniquement au contrôle d'édition.</span><span class="sxs-lookup"><span data-stu-id="416f6-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="416f6-142">Les contrôles qui n'autorisent pas l'entrée de l'utilisateur, tels qu'un bouton ou une étiquette, définissent 0 pour leurs indicateurs de contrôle.</span><span class="sxs-lookup"><span data-stu-id="416f6-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="416f6-143">De nombreuses valeurs d'indicateur sont explicites.</span><span class="sxs-lookup"><span data-stu-id="416f6-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="416f6-144">Par exemple, lorsque DT_REQUIRED est défini pour un contrôle, il doit contenir une valeur pour que la boîte de dialogue ne soit pas autorisée à être fermée.</span><span class="sxs-lookup"><span data-stu-id="416f6-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="416f6-145">Le fournisseur de services peut fournir une valeur par le biais de son implémentation **IMAPIProp** ou l'utilisateur peut en entrer un.</span><span class="sxs-lookup"><span data-stu-id="416f6-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="416f6-146">DT_EDITABLE indique que la valeur du contrôle peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="416f6-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="416f6-147">DT_MULTILINE permet à la valeur d'un contrôle d'édition de s'étendre sur plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="416f6-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="416f6-148">Certains indicateurs de contrôle ne sont pas si évidents dans leur sens.</span><span class="sxs-lookup"><span data-stu-id="416f6-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="416f6-149">Lorsqu'un contrôle définit l'indicateur DT_SET_IMMEDIATE, toutes les modifications apportées à sa valeur prennent effet dès que l'utilisateur passe à un nouveau contrôle.</span><span class="sxs-lookup"><span data-stu-id="416f6-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="416f6-150">MAPI effectue un seul appel à la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de l'interface de propriété pour la propriété du contrôle.</span><span class="sxs-lookup"><span data-stu-id="416f6-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="416f6-151">Cela est différent du comportement par défaut, qui consiste à différer que les modifications apportées aux valeurs de contrôle prennent effet jusqu'à ce que l'utilisateur sélectionne le bouton **OK** ou ferme la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="416f6-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="416f6-152">L'indicateur DT_SET_IMMEDIATE est souvent utilisé en combinaison avec des notifications de table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="416f6-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="416f6-153">Le tableau suivant répertorie les types de contrôles et toutes les valeurs d'indicateur pouvant être définies pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="416f6-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="416f6-154">**Contrôle**</span><span class="sxs-lookup"><span data-stu-id="416f6-154">**Control**</span></span>|<span data-ttu-id="416f6-155">**Valeurs valides pour cette propriété**</span><span class="sxs-lookup"><span data-stu-id="416f6-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="416f6-156">Bouton</span><span class="sxs-lookup"><span data-stu-id="416f6-156">Button</span></span>  <br/> |<span data-ttu-id="416f6-157">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-158">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="416f6-158">Check box</span></span>  <br/> |<span data-ttu-id="416f6-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="416f6-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="416f6-160">Zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="416f6-160">Combo box</span></span>  <br/> |<span data-ttu-id="416f6-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="416f6-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="416f6-162">Zone de liste déRoulante</span><span class="sxs-lookup"><span data-stu-id="416f6-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="416f6-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="416f6-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="416f6-164">Modifier</span><span class="sxs-lookup"><span data-stu-id="416f6-164">Edit</span></span>  <br/> |<span data-ttu-id="416f6-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="416f6-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="416f6-166">Zone de groupe</span><span class="sxs-lookup"><span data-stu-id="416f6-166">Group box</span></span>  <br/> |<span data-ttu-id="416f6-167">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-168">Étiquette</span><span class="sxs-lookup"><span data-stu-id="416f6-168">Label</span></span>  <br/> |<span data-ttu-id="416f6-169">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-170">Zone de liste</span><span class="sxs-lookup"><span data-stu-id="416f6-170">List box</span></span>  <br/> |<span data-ttu-id="416f6-171">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-172">Zone de liste déroulante à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="416f6-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="416f6-173">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-174">Zone de liste à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="416f6-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="416f6-175">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-176">Page à onglets</span><span class="sxs-lookup"><span data-stu-id="416f6-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="416f6-177">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="416f6-178">Case d'option</span><span class="sxs-lookup"><span data-stu-id="416f6-178">Radio button</span></span>  <br/> |<span data-ttu-id="416f6-179">Doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="416f6-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="416f6-180">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="416f6-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="416f6-181">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="416f6-181">Header files</span></span>

<span data-ttu-id="416f6-182">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="416f6-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="416f6-183">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="416f6-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="416f6-184">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="416f6-184">Mapitags.h</span></span>
  
> <span data-ttu-id="416f6-185">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="416f6-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="416f6-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="416f6-186">See also</span></span>



[<span data-ttu-id="416f6-187">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="416f6-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="416f6-188">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="416f6-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="416f6-189">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="416f6-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="416f6-190">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="416f6-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

