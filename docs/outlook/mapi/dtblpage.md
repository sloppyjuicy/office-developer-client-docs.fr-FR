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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340116"
---
# <a name="dtblpage"></a><span data-ttu-id="31646-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="31646-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="31646-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31646-105">Décrit une page à onglets qui sera utilisée dans une boîte de dialogue construite à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="31646-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31646-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="31646-106">Header file:</span></span>  <br/> |<span data-ttu-id="31646-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="31646-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="31646-108">Macro connexe:</span><span class="sxs-lookup"><span data-stu-id="31646-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="31646-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="31646-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="31646-110">Members</span><span class="sxs-lookup"><span data-stu-id="31646-110">Members</span></span>

 <span data-ttu-id="31646-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="31646-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="31646-112">Position en mémoire de l'étiquette de la chaîne de caractères pour l'onglet page.</span><span class="sxs-lookup"><span data-stu-id="31646-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="31646-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="31646-113">**ulFlags**</span></span>
  
> <span data-ttu-id="31646-114">Masque de des indicateurs utilisé pour désigner le format de l'étiquette désignée par le membre **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="31646-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="31646-115">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="31646-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="31646-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="31646-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="31646-117">L'étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="31646-117">The label is in Unicode format.</span></span> <span data-ttu-id="31646-118">Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="31646-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="31646-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="31646-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="31646-120">Position en mémoire d'une chaîne de caractères identifiant la section **[Help file Mappings] du fichier** MAPISVC. Fichier de configuration INF ou 0.</span><span class="sxs-lookup"><span data-stu-id="31646-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="31646-121">Nom de fichier apparaissant dans le fichier MAPISVC. INF peut être utilisée par un utilisateur pour accéder à une aide étendue pour la page à onglets en cliquant sur le bouton **aide** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="31646-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="31646-122">Pour plus d'informations sur les entrées dans MAPISVC. INF, consultez le [format de fichier MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="31646-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="31646-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="31646-123">**ulContext**</span></span>
  
> <span data-ttu-id="31646-124">Identificateur unique de la page à onglets dans la chaîne définie par le membre **ulbLpszComponent** .</span><span class="sxs-lookup"><span data-stu-id="31646-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="31646-125">Le membre **ulbLpszComponent** et le membre **ulContext** doivent avoir une valeur différente de zéro pour que le bouton **aide** fonctionne.</span><span class="sxs-lookup"><span data-stu-id="31646-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="31646-126">Si cet identificateur est égal à zéro et que la chaîne du composant est NULL, aucune aide n'est associée à la page.</span><span class="sxs-lookup"><span data-stu-id="31646-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31646-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="31646-127">Remarks</span></span>

<span data-ttu-id="31646-128">Une structure **DTBLPAGE** décrit une page à onglets qui est un contrôle utilisé pour séparer plusieurs boîtes de dialogue associées.</span><span class="sxs-lookup"><span data-stu-id="31646-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="31646-129">En règle générale, ces boîtes de dialogue sont des feuilles de propriétés permettant d'afficher les options de configuration, de message ou de destinataire.</span><span class="sxs-lookup"><span data-stu-id="31646-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="31646-130">En cliquant sur l'onglet, l'utilisateur peut passer d'une feuille à une autre.</span><span class="sxs-lookup"><span data-stu-id="31646-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="31646-131">La chaîne de composant et l'identificateur de contexte fournissent des informations indiquant si l'aide étendue est disponible pour la page à onglets.</span><span class="sxs-lookup"><span data-stu-id="31646-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="31646-132">Si l'aide étendue est disponible, la chaîne de composant et l'identificateur de contexte fournissent des informations sur la façon d'y accéder.</span><span class="sxs-lookup"><span data-stu-id="31646-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="31646-133">La chaîne de composant est mappée sur le fichier d'aide; l'identificateur de contexte correspond à la rubrique d'aide initiale.</span><span class="sxs-lookup"><span data-stu-id="31646-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="31646-134">Si l'identificateur de contexte est zéro et que la chaîne de composant est NULL, l'aide étendue n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="31646-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="31646-135">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="31646-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="31646-136">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="31646-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31646-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31646-137">See also</span></span>



[<span data-ttu-id="31646-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="31646-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="31646-139">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="31646-139">MAPI Structures</span></span>](mapi-structures.md)

