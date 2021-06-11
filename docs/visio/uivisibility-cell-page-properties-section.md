---
title: UIVisibility, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437328"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="9782d-103">UIVisibility, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="9782d-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="9782d-104">Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="9782d-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="9782d-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9782d-105">**Value**</span></span>|<span data-ttu-id="9782d-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="9782d-106">**Description**</span></span>|<span data-ttu-id="9782d-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="9782d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9782d-108">0</span><span class="sxs-lookup"><span data-stu-id="9782d-108">0</span></span>  <br/> |<span data-ttu-id="9782d-109">Affiche le nom de la page dans l'IU (par défaut).</span><span class="sxs-lookup"><span data-stu-id="9782d-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="9782d-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="9782d-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="9782d-111">1</span><span class="sxs-lookup"><span data-stu-id="9782d-111">1</span></span>  <br/> |<span data-ttu-id="9782d-112">N'affiche pas le nom de la page dans l'IU.</span><span class="sxs-lookup"><span data-stu-id="9782d-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="9782d-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="9782d-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9782d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9782d-114">Remarks</span></span>

<span data-ttu-id="9782d-115">Définir la cellule UIVisibility sur **visUIVHidden** empêche la page d’apparaître n’importe où dans l’interface utilisateur où la chaîne contenant le nom de la page apparaît.</span><span class="sxs-lookup"><span data-stu-id="9782d-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="9782d-116">Par exemple, la page ne serait pas présentée comme option dans l’**Explorateur de dessin** ou dans les onglets de page.</span><span class="sxs-lookup"><span data-stu-id="9782d-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="9782d-117">La page reste toutefois accessible si vous utilisez automation ou des chemins d’accès d’interface utilisateur qui n’incluent pas le nom de la page, par exemple, la commande **Imprimer.**</span><span class="sxs-lookup"><span data-stu-id="9782d-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="9782d-118">Cette cellule est destinée à être utilisée uniquement avec des pages de document  elle n'est pas destinée à être utilisée avec des pages de superposition de marque de révision, dont la cellule UIVisibility est définie par défaut sur **visUIVHidden** et ne doit pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="9782d-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9782d-119">Pour masquer une page de  la commande Imprimer du document, faites-en une page d’arrière-plan (la propriété **Type** est **visTypeBackground)** qui n’est utilisée comme arrière-plan par aucune page (les formes des pages d’arrière-plan sont imprimées lorsqu’une page l’utilise en arrière-plan).</span><span class="sxs-lookup"><span data-stu-id="9782d-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="9782d-120">La commande Imprimer **du** document fonctionne uniquement avec les pages indexées et les pages d’arrière-plan ne sont pas indexées.</span><span class="sxs-lookup"><span data-stu-id="9782d-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="9782d-121">Pour obtenir une référence à la cellule UIVisibility par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9782d-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9782d-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9782d-122">Cell name:</span></span>  <br/> |<span data-ttu-id="9782d-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="9782d-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="9782d-124">Pour obtenir une référence à la cellule UIVisibility à l'aide d'un index à partir un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9782d-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9782d-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9782d-125">Section index:</span></span>  <br/> |<span data-ttu-id="9782d-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9782d-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9782d-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9782d-127">Row index:</span></span>  <br/> |<span data-ttu-id="9782d-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="9782d-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="9782d-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9782d-129">Cell index:</span></span>  <br/> |<span data-ttu-id="9782d-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="9782d-130">**visPageUIVisibility**</span></span> <br/> |
   

