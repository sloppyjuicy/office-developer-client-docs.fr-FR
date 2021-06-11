---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421500"
---
# <a name="dtctl"></a><span data-ttu-id="6e2ab-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="6e2ab-103">DTCTL</span></span>

<span data-ttu-id="6e2ab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e2ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e2ab-105">Décrit un contrôle qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e2ab-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6e2ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e2ab-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e2ab-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a><span data-ttu-id="6e2ab-108">Members</span><span class="sxs-lookup"><span data-stu-id="6e2ab-108">Members</span></span>

<span data-ttu-id="6e2ab-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="6e2ab-110">Type de contrôle qui est inclus dans le membre **ctl** et correspond à la propriété PR_CONTROL_TYPE **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="6e2ab-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e2ab-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="6e2ab-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="6e2ab-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="6e2ab-113">Contrôle Étiquette</span><span class="sxs-lookup"><span data-stu-id="6e2ab-113">Label control.</span></span>
    
<span data-ttu-id="6e2ab-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="6e2ab-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="6e2ab-115">Contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-115">Edit control.</span></span>
    
<span data-ttu-id="6e2ab-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="6e2ab-117">Contrôle Zone de liste.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-117">List box control.</span></span>
    
<span data-ttu-id="6e2ab-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="6e2ab-119">Contrôle Zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-119">Combo box control.</span></span>
    
<span data-ttu-id="6e2ab-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="6e2ab-121">Contrôle de liste liste de listes.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-121">Drop-down list control.</span></span>
    
<span data-ttu-id="6e2ab-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="6e2ab-123">Contrôle Case à cocher.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-123">Check box control.</span></span>
    
<span data-ttu-id="6e2ab-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="6e2ab-125">Contrôle zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-125">Group box control.</span></span>
    
<span data-ttu-id="6e2ab-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="6e2ab-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="6e2ab-127">Contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-127">Button control.</span></span>
    
<span data-ttu-id="6e2ab-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="6e2ab-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="6e2ab-129">Contrôle de page à onglets.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-129">Tabbed page control.</span></span>
    
<span data-ttu-id="6e2ab-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="6e2ab-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="6e2ab-131">Contrôle de bouton d’radio.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-131">Radio button control.</span></span>
    
<span data-ttu-id="6e2ab-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="6e2ab-133">Contrôle de liste à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="6e2ab-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="6e2ab-135">Contrôle de listes de listes listes à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="6e2ab-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="6e2ab-137">Masque de bits d’indicateurs qui décrit les fonctionnalités du contrôle et correspond à la propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6e2ab-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="6e2ab-138">Ces indicateurs peuvent être définies pour les cases à cocher, les zones de liste déroulante, les zones de liste et les contrôles de modification uniquement.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="6e2ab-139">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e2ab-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="6e2ab-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="6e2ab-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="6e2ab-141">Le format ANSI ou DBCS est accepté.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="6e2ab-142">Cet indicateur est valide pour les contrôles d’édition uniquement.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="6e2ab-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="6e2ab-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="6e2ab-144">Un utilisateur peut modifier le texte du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="6e2ab-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="6e2ab-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="6e2ab-146">Le contrôle peut contenir plusieurs lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="6e2ab-147">Cet indicateur est valide pour les contrôles d’édition uniquement.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="6e2ab-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="6e2ab-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="6e2ab-149">Le contrôle contient un mot de passe ; par conséquent, le contenu du contrôle ne doit pas être affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="6e2ab-150">Cet indicateur est valide pour les contrôles d’édition uniquement.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="6e2ab-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="6e2ab-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="6e2ab-152">Le contrôle de boîte de dialogue est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-152">The dialog box control is required.</span></span> <span data-ttu-id="6e2ab-153">Cet indicateur est valide uniquement pour les contrôles de zone de liste modifiable et de modification.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="6e2ab-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="6e2ab-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="6e2ab-155">Active la sortie immédiate d’une valeur en cas de modification du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="6e2ab-156">Cela permet d’établir une relation de dépendance entre deux contrôles.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="6e2ab-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="6e2ab-158">Pointeur vers une structure constituée d’une structure [GUID,](guid.md) pour représenter le fournisseur de services et un identificateur pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="6e2ab-159">Les membres **lpbNotif** et **cbNotif** correspondent à la propriété **PR_CONTROL_ID (** [PidTagControlId](pidtagcontrolid-canonical-property.md)) du contrôle et sont utilisés pour avertir l’interface utilisateur lorsque le contrôle doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="6e2ab-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-160">**cbNotif**</span></span>
  
> <span data-ttu-id="6e2ab-161">Nombre d’octets dans la structure pointée par **le membre lpbNotif.**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="6e2ab-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="6e2ab-163">Pointeur vers une chaîne de caractères qui décrit les caractères qui peuvent être entrés dans un contrôle de zone de liste modifiable ou modifiable.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="6e2ab-164">Pour d’autres types de contrôles, le **membre lpszFilter** peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="6e2ab-165">Pour les contrôles d’édition et de zone de liste déroulante, il doit s’agit d’une expression régulière qui s’applique à un seul caractère à la fois.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="6e2ab-166">Le même filtre est appliqué à tous les caractères du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="6e2ab-167">Le format de la chaîne de filtre est le suivant :</span><span class="sxs-lookup"><span data-stu-id="6e2ab-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="6e2ab-168">**Caractère**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-168">**Character**</span></span>|<span data-ttu-id="6e2ab-169">**Description**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="6e2ab-170">Tout caractère est autorisé (par exemple, `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="6e2ab-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="6e2ab-171">Définit un ensemble de caractères (par exemple, `"[0123456789]"` .)</span><span class="sxs-lookup"><span data-stu-id="6e2ab-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="6e2ab-172">Indique une plage de caractères (par exemple, `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="6e2ab-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="6e2ab-173">Indique que ces caractères ne sont pas autorisés (par exemple, `"[~0-9]")` .</span><span class="sxs-lookup"><span data-stu-id="6e2ab-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="6e2ab-174">Utilisé pour guillemets l’un des symboles précédents (par exemple, les caractères `"[\-\\\[\]]"` -, \, [et ] sont autorisés).</span><span class="sxs-lookup"><span data-stu-id="6e2ab-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="6e2ab-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-175">**ulItemID**</span></span>
  
> <span data-ttu-id="6e2ab-176">Valeur qui identifie le contrôle dans la ressource de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="6e2ab-177">Pour les contrôles de pages à onglets de type DTCT_PAGE le membre **ulItemID** est éventuellement utilisé pour charger le nom du composant de la page à partir d’une ressource de chaîne.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="6e2ab-178">Les informations de position et d’étiquette sont lues à partir de la ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="6e2ab-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-179">**ctl**</span></span>
  
> <span data-ttu-id="6e2ab-180">Structure qui contient les données du contrôle et correspond à la propriété PR_CONTROL_STRUCTURE **(** [PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6e2ab-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="6e2ab-181">Chaque type de contrôle a une structure différente.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e2ab-182">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e2ab-182">Remarks</span></span>

<span data-ttu-id="6e2ab-183">La structure **DTCTL** décrit un contrôle de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="6e2ab-184">La plupart de ses membres sont utilisés pour définir des propriétés sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="6e2ab-185">Le **membre ctl** est une union de structures liées à un type particulier de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="6e2ab-186">Si la structure **DTCTL** décrit un contrôle d’édition, par exemple, le membre **ctl** pointe vers une structure [DTBLEDIT.](dtbledit.md)</span><span class="sxs-lookup"><span data-stu-id="6e2ab-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="6e2ab-187">Cette structure correspond à la propriété PR_CONTROL_STRUCTURE **du** contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="6e2ab-188">L’union possède comme premier membre une variable de type LPVOID pour permettre l’initialisation du temps de compilation de la structure **DTCTL.**</span><span class="sxs-lookup"><span data-stu-id="6e2ab-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="6e2ab-189">Bien que la [fonction BuildDisplayTable](builddisplaytable.md) utilise la structure **DTCTL** pour créer la table d’affichage à partir des ressources de contrôle, la structure **DTCTL** n’apparaît jamais dans le tableau d’affichage lui-même.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="6e2ab-190">Cette structure fournit simplement des informations **à BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="6e2ab-191">Dans le **membre ulCtlFlags,** quatre indicateurs DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT les contrôles d’édition uniquement.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="6e2ab-192">Deux autres DT_REQUIRED et DT_SET_IMMEDIATE un contrôle modifiable.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="6e2ab-193">Les contrôles disponibles pour une boîte de dialogue sont étiquette, zone de texte, zone de texte sensible à l’encre, liste, liste déroulante, zone de liste déroulante, case à cocher, zone de groupe, bouton, case d’radio et page à onglets.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="6e2ab-194">Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6e2ab-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="6e2ab-195">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="6e2ab-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e2ab-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e2ab-196">See also</span></span>

- [<span data-ttu-id="6e2ab-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="6e2ab-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="6e2ab-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="6e2ab-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="6e2ab-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="6e2ab-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="6e2ab-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="6e2ab-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="6e2ab-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="6e2ab-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="6e2ab-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="6e2ab-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="6e2ab-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="6e2ab-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="6e2ab-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="6e2ab-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="6e2ab-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="6e2ab-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="6e2ab-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="6e2ab-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="6e2ab-210">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="6e2ab-210">MAPI Structures</span></span>](mapi-structures.md)

