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
# <a name="dtctl"></a><span data-ttu-id="f1c4d-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f1c4d-103">DTCTL</span></span>

<span data-ttu-id="f1c4d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1c4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1c4d-105">Décrit un contrôle qui sera utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1c4d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f1c4d-106">Header file:</span></span>  <br/> |<span data-ttu-id="f1c4d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f1c4d-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f1c4d-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1c4d-108">Members</span></span>

<span data-ttu-id="f1c4d-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="f1c4d-110">Type de contrôle inclus dans le membre **CTL** et correspondant à la propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="f1c4d-111">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="f1c4d-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="f1c4d-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="f1c4d-113">Contrôle Étiquette</span><span class="sxs-lookup"><span data-stu-id="f1c4d-113">Label control.</span></span>
    
<span data-ttu-id="f1c4d-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="f1c4d-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="f1c4d-115">Contrôle d'édition.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-115">Edit control.</span></span>
    
<span data-ttu-id="f1c4d-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="f1c4d-117">Contrôle zone de liste.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-117">List box control.</span></span>
    
<span data-ttu-id="f1c4d-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="f1c4d-119">Contrôle de zone de liste déRoulante.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-119">Combo box control.</span></span>
    
<span data-ttu-id="f1c4d-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="f1c4d-121">Contrôle de liste déRoulante.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-121">Drop-down list control.</span></span>
    
<span data-ttu-id="f1c4d-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="f1c4d-123">Contrôle case à coCher.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-123">Check box control.</span></span>
    
<span data-ttu-id="f1c4d-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="f1c4d-125">Contrôle de zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-125">Group box control.</span></span>
    
<span data-ttu-id="f1c4d-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="f1c4d-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="f1c4d-127">Contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-127">Button control.</span></span>
    
<span data-ttu-id="f1c4d-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="f1c4d-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="f1c4d-129">Contrôle page à onglets.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-129">Tabbed page control.</span></span>
    
<span data-ttu-id="f1c4d-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="f1c4d-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="f1c4d-131">Contrôle de case d'option.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-131">Radio button control.</span></span>
    
<span data-ttu-id="f1c4d-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="f1c4d-133">Contrôle de liste à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="f1c4d-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="f1c4d-135">Contrôle de liste déroulante à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="f1c4d-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="f1c4d-137">Masque de des indicateurs qui décrit les fonctionnalités du contrôle et correspond à la propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="f1c4d-138">Ces indicateurs peuvent être définis pour les cases à cocher, les zones de liste déroulante, les zones de liste et les contrôles d'édition uniquement.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="f1c4d-139">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="f1c4d-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="f1c4d-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="f1c4d-141">Le format ANSI ou DBCS est accepté.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="f1c4d-142">Cet indicateur est valide uniquement pour les contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="f1c4d-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="f1c4d-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="f1c4d-144">Un utilisateur peut modifier le texte dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="f1c4d-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="f1c4d-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="f1c4d-146">Le contrôle peut contenir plusieurs lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="f1c4d-147">Cet indicateur est valide uniquement pour les contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="f1c4d-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="f1c4d-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="f1c4d-149">Le contrôle contient un mot de passe; par conséquent, le contenu du contrôle ne doit pas être affiché à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="f1c4d-150">Cet indicateur est valide uniquement pour les contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="f1c4d-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="f1c4d-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="f1c4d-152">Le contrôle de la boîte de dialogue est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-152">The dialog box control is required.</span></span> <span data-ttu-id="f1c4d-153">Cet indicateur est valide uniquement pour les contrôles de zone de liste modifiable et de modification.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="f1c4d-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="f1c4d-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="f1c4d-155">Active la sortie immédiate d'une valeur lors d'une modification dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="f1c4d-156">Cela permet d'établir une relation de dépendance entre deux contrôles.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="f1c4d-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="f1c4d-158">Pointeur vers une structure qui se compose d'une structure de [GUID](guid.md) , pour représenter le fournisseur de services et un identificateur pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="f1c4d-159">Les membres **lpbNotif** et **cbNotif** correspondent à la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) du contrôle et sont utilisés pour avertir l'interface utilisateur lorsque le contrôle doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="f1c4d-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-160">**cbNotif**</span></span>
  
> <span data-ttu-id="f1c4d-161">Nombre d'octets dans la structure vers laquelle pointe le membre **lpbNotif** .</span><span class="sxs-lookup"><span data-stu-id="f1c4d-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="f1c4d-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="f1c4d-163">Pointeur vers une chaîne de caractères qui décrit quels caractères peuvent être saisis dans un contrôle de zone de liste modifiable ou de modification.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="f1c4d-164">Pour les autres types de contrôles, le membre **lpszFilter** peut être null.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="f1c4d-165">Pour les contrôles de zone de liste modifiable et de zone de liste modifiable, il doit s'agir d'une expression régulière qui s'applique à un seul caractère à la fois.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="f1c4d-166">Le même filtre est appliqué à tous les caractères dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="f1c4d-167">Le format de la chaîne de filtrage est le suivant:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="f1c4d-168">**Caractère**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-168">**Character**</span></span>|<span data-ttu-id="f1c4d-169">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="f1c4d-170">N'importe quel caractère est autorisé (par `"*"`exemple,).</span><span class="sxs-lookup"><span data-stu-id="f1c4d-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="f1c4d-171">Définit un jeu de caractères (par exemple, `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="f1c4d-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="f1c4d-172">Indique une plage de caractères (par exemple, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="f1c4d-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="f1c4d-173">Indique que ces caractères ne sont pas autorisés (par exemple `"[~0-9]")`,.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="f1c4d-174">Utilisé pour citer tous les symboles précédents (par exemple, `"[\-\\\[\]]"` les caractères «, \, » et «») sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="f1c4d-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-175">**ulItemID**</span></span>
  
> <span data-ttu-id="f1c4d-176">Valeur qui identifie le contrôle dans la ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="f1c4d-177">Pour les contrôles de pages à onglets de type DTCT_PAGE, le membre **ulItemID** est éventuellement utilisé pour charger le nom du composant de la page à partir d'une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="f1c4d-178">Les informations sur la position et l'étiquette sont lues à partir de la ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="f1c4d-179">**CTL**</span><span class="sxs-lookup"><span data-stu-id="f1c4d-179">**ctl**</span></span>
  
> <span data-ttu-id="f1c4d-180">Structure qui contient les données du contrôle et correspond à la propriété **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="f1c4d-181">Chaque type de contrôle a une structure différente.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1c4d-182">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1c4d-182">Remarks</span></span>

<span data-ttu-id="f1c4d-183">La structure **DTCTL** décrit un contrôle de n'importe quel type.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="f1c4d-184">La plupart de ses membres sont utilisés pour définir des propriétés sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="f1c4d-185">Le membre **CTL** est une Union de structures qui se rapportent à un type de contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="f1c4d-186">Si la structure **DTCTL** décrit un contrôle d'édition, par exemple, le membre de la **liste de certificats de confiance** pointe vers une structure [DTBLEDIT](dtbledit.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c4d-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="f1c4d-187">Cette structure correspond à la propriété **PR_CONTROL_STRUCTURE** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="f1c4d-188">L'Union a comme premier membre une variable de type LPVOID pour permettre l'initialisation au moment de la compilation de la structure **DTCTL** .</span><span class="sxs-lookup"><span data-stu-id="f1c4d-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="f1c4d-189">Bien que la fonction [BuildDisplayTable](builddisplaytable.md) utilise la structure **DTCTL** pour créer la table d'affichage à partir des ressources de contrôle, la structure **DTCTL** n'apparaît jamais dans le tableau d'affichage proprement dit.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="f1c4d-190">Cette structure fournit des informations à **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="f1c4d-191">Dans le membre **ulCtlFlags** , quatre indicateurs DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affectent uniquement les contrôles d'édition.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="f1c4d-192">Deux autres DT_REQUIRED et DT_SET_IMMEDIATE affectent tous les contrôles modifiables.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="f1c4d-193">Les contrôles disponibles pour une boîte de dialogue sont étiquette, zone de texte, zone de texte prenant en charge l'entrée manuscrite, liste, liste déroulante, zone de liste déroulante, zone de groupe, bouton, case d'option et page à onglets.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="f1c4d-194">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f1c4d-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f1c4d-195">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f1c4d-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1c4d-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1c4d-196">See also</span></span>

- [<span data-ttu-id="f1c4d-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="f1c4d-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="f1c4d-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="f1c4d-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="f1c4d-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="f1c4d-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="f1c4d-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="f1c4d-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="f1c4d-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="f1c4d-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="f1c4d-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="f1c4d-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="f1c4d-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="f1c4d-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="f1c4d-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="f1c4d-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="f1c4d-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="f1c4d-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="f1c4d-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="f1c4d-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="f1c4d-210">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="f1c4d-210">MAPI Structures</span></span>](mapi-structures.md)

