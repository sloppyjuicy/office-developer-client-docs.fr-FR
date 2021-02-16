---
title: LockCustProp, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Détermine si l’utilisateur peut ajouter, supprimer ou modifier des données de forme dans l’interface utilisateur à l’aide de la boîte de dialogue Définir les données de forme ou du menu contextuel de la fenêtre Données de forme.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422522"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="08b4b-103">LockCustProp, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="08b4b-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="08b4b-104">Détermine si l’utilisateur peut ajouter, supprimer ou modifier des données de forme dans l’interface utilisateur à l’aide de la boîte de dialogue **Définir les données de forme** ou du menu contextuel de la fenêtre **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="08b4b-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="08b4b-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="08b4b-105">**Value**</span></span>|<span data-ttu-id="08b4b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="08b4b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08b4b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="08b4b-107">TRUE</span></span>  <br/> |<span data-ttu-id="08b4b-108">La commande **Définir les données de forme** dans le menu contextuel de la fenêtre **Données de forme** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="08b4b-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="08b4b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="08b4b-109">FALSE</span></span>  <br/> |<span data-ttu-id="08b4b-110">La commande **Définir les données de forme** dans le menu contextuel de la fenêtre **Données de forme** est activée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="08b4b-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08b4b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="08b4b-111">Remarks</span></span>

<span data-ttu-id="08b4b-112">La valeur TRUE n'empêche pas un utilisateur de changer la valeur d'un élément de données de forme ni de modifier la section Données de forme de la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="08b4b-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="08b4b-113">Pour obtenir une référence à la cellule LockCustProp par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="08b4b-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08b4b-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="08b4b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="08b4b-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="08b4b-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="08b4b-116">Pour obtenir une référence à la cellule LockCustProp à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="08b4b-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08b4b-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="08b4b-117">Section index:</span></span>  <br/> |<span data-ttu-id="08b4b-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08b4b-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="08b4b-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="08b4b-119">Row index:</span></span>  <br/> |<span data-ttu-id="08b4b-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="08b4b-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="08b4b-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="08b4b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="08b4b-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="08b4b-122">**visLockCustProp**</span></span> <br/> |
   

