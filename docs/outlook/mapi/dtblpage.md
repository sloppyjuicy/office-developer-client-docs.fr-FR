---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bd0caff8a6c7834bdd01ef4be64805bde66dd6d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578821"
---
# <a name="dtblpage"></a><span data-ttu-id="80dd8-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="80dd8-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="80dd8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80dd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80dd8-105">Décrit une page à onglets qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="80dd8-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80dd8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="80dd8-106">Header file:</span></span>  <br/> |<span data-ttu-id="80dd8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80dd8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="80dd8-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="80dd8-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="80dd8-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="80dd8-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="80dd8-110">Members</span><span class="sxs-lookup"><span data-stu-id="80dd8-110">Members</span></span>

 <span data-ttu-id="80dd8-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="80dd8-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="80dd8-112">Position dans la mémoire de l’étiquette de chaîne de caractères de l’onglet page.</span><span class="sxs-lookup"><span data-stu-id="80dd8-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="80dd8-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="80dd8-113">**ulFlags**</span></span>
  
> <span data-ttu-id="80dd8-114">Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="80dd8-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="80dd8-115">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="80dd8-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="80dd8-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80dd8-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="80dd8-117">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="80dd8-117">The label is in Unicode format.</span></span> <span data-ttu-id="80dd8-118">Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="80dd8-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="80dd8-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="80dd8-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="80dd8-120">Position dans la mémoire d’une chaîne de caractères identifiant la section **[Help File Mappings]** dans le fichier MAPISVC.inf. Fichier configuration ou 0.</span><span class="sxs-lookup"><span data-stu-id="80dd8-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="80dd8-121">Le nom de fichier figurant dans le fichier MAPISVC.inf. Section INF peut être utilisée par un utilisateur à accéder à l’aide étendue pour la page à onglets en cliquant sur le bouton **aide** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="80dd8-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="80dd8-122">Pour plus d’informations sur les entrées dans le fichier MAPISVC.inf. INF, voir [Format de fichier du fichier MAPISVC.inf. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="80dd8-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="80dd8-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="80dd8-123">**ulContext**</span></span>
  
> <span data-ttu-id="80dd8-124">Identificateur unique de la page à onglets dans la chaîne définie par le membre **ulbLpszComponent** .</span><span class="sxs-lookup"><span data-stu-id="80dd8-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="80dd8-125">Le membre **ulbLpszComponent** et le membre **ulContext** doivent être différent de zéro pour le bouton **aide** travailler.</span><span class="sxs-lookup"><span data-stu-id="80dd8-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="80dd8-126">Si cet identificateur est égale à zéro, et la chaîne du composant est NULL, aucune aide n’est associée à la page.</span><span class="sxs-lookup"><span data-stu-id="80dd8-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="80dd8-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="80dd8-127">Remarks</span></span>

<span data-ttu-id="80dd8-128">Une structure **DTBLPAGE** décrit une page à onglets un contrôle qui est utilisé pour séparer plusieurs boîtes de dialogue connexes.</span><span class="sxs-lookup"><span data-stu-id="80dd8-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="80dd8-129">En règle générale, ces boîtes de dialogue sont des feuilles de propriétés pour afficher les options pour le destinataire, message ou configuration.</span><span class="sxs-lookup"><span data-stu-id="80dd8-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="80dd8-130">En cliquant sur l’onglet, l’utilisateur peut passer d’une feuille à une autre.</span><span class="sxs-lookup"><span data-stu-id="80dd8-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="80dd8-131">L’identificateur de chaîne et le contexte du composant fournissent des informations sur si aide détaillée est disponible pour la page à onglets.</span><span class="sxs-lookup"><span data-stu-id="80dd8-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="80dd8-132">Si aide détaillée est disponible, l’identificateur de chaîne et le contexte de composant fournit des informations sur la façon d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="80dd8-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="80dd8-133">La chaîne composant mappe sur le fichier d’aide ; l’ID de contexte correspond à la rubrique d’aide.</span><span class="sxs-lookup"><span data-stu-id="80dd8-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="80dd8-134">Si l’ID de contexte est égale à zéro, et la chaîne du composant est NULL, aide étendue n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="80dd8-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="80dd8-135">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="80dd8-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="80dd8-136">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="80dd8-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80dd8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80dd8-137">See also</span></span>



[<span data-ttu-id="80dd8-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="80dd8-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="80dd8-139">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="80dd8-139">MAPI Structures</span></span>](mapi-structures.md)

