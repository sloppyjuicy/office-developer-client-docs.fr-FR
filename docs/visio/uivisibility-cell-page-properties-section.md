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
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789988"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="1e58e-103">UIVisibility, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="1e58e-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="1e58e-104">Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="1e58e-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="1e58e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1e58e-105">**Value**</span></span>|<span data-ttu-id="1e58e-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="1e58e-106">**Description**</span></span>|<span data-ttu-id="1e58e-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="1e58e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e58e-108">0</span><span class="sxs-lookup"><span data-stu-id="1e58e-108">0</span></span>  <br/> |<span data-ttu-id="1e58e-109">Affiche le nom de la page dans l'IU (par défaut).</span><span class="sxs-lookup"><span data-stu-id="1e58e-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="1e58e-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="1e58e-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="1e58e-111">1</span><span class="sxs-lookup"><span data-stu-id="1e58e-111">1</span></span>  <br/> |<span data-ttu-id="1e58e-112">N'affiche pas le nom de la page dans l'IU.</span><span class="sxs-lookup"><span data-stu-id="1e58e-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="1e58e-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="1e58e-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e58e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e58e-114">Remarks</span></span>

<span data-ttu-id="1e58e-115">Définir la cellule UIVisibility sur **visUIVHidden** empêche la page d’apparaître n’importe où dans l’interface utilisateur où la chaîne contenant le nom de la page s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1e58e-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="1e58e-116">Par exemple, la page ne serait pas figurer en tant qu’option dans l' **Explorateur de dessins** ou sur les onglets de page.</span><span class="sxs-lookup"><span data-stu-id="1e58e-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="1e58e-117">La page reste accessible, toutefois, si vous utilisez des chemins d’accès Automation ou l’interface utilisateur qui n’incluent pas le nom de la page, par exemple, la commande **Imprimer** .</span><span class="sxs-lookup"><span data-stu-id="1e58e-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="1e58e-118">Cette cellule est destinée aux pages du document ; Il n’est pas destiné à utiliser avec les pages de superposition de balisage, dont la cellule UIVisibility sur **visUIVHidden** la valeur par défaut et ne doit pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="1e58e-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1e58e-119">Pour masquer une page à partir de la commande **d’impression** du document, faites-en une page d’arrière-plan (la propriété**Type** est **visTypeBackground** ) qui n’est pas utilisé en tant qu’arrière-plan par n’importe quelle page (les formes sur les pages d’arrière-plan sont imprimées lorsqu’une page à l’utiliser en tant qu’arrière-plan est impression).</span><span class="sxs-lookup"><span data-stu-id="1e58e-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="1e58e-120">Commande **d’impression** du document ne fonctionne qu’avec des pages indexées et les pages d’arrière-plan ne sont pas indexés.</span><span class="sxs-lookup"><span data-stu-id="1e58e-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="1e58e-121">Pour obtenir une référence à la cellule UIVisibility par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="1e58e-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e58e-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1e58e-122">Cell name:</span></span>  <br/> |<span data-ttu-id="1e58e-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="1e58e-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="1e58e-124">Pour obtenir une référence à la cellule UIVisibility par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1e58e-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e58e-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1e58e-125">Section index:</span></span>  <br/> |<span data-ttu-id="1e58e-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1e58e-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1e58e-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1e58e-127">Row index:</span></span>  <br/> |<span data-ttu-id="1e58e-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="1e58e-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="1e58e-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1e58e-129">Cell index:</span></span>  <br/> |<span data-ttu-id="1e58e-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="1e58e-130">**visPageUIVisibility**</span></span> <br/> |
   

