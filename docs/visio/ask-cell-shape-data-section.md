---
title: Ask, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341439"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="7567a-103">Ask, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="7567a-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="7567a-104">Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.</span><span class="sxs-lookup"><span data-stu-id="7567a-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="7567a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="7567a-105">**Value**</span></span>|<span data-ttu-id="7567a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7567a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7567a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7567a-107">TRUE</span></span>  <br/> |<span data-ttu-id="7567a-108">L'utilisateur est invité à entrer des données de forme dans la boîte de dialogue **Définir les données de forme**.</span><span class="sxs-lookup"><span data-stu-id="7567a-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="7567a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7567a-109">FALSE</span></span>  <br/> |<span data-ttu-id="7567a-110">L'utilisateur n'est pas invité à entrer de données.</span><span class="sxs-lookup"><span data-stu-id="7567a-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7567a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="7567a-111">Remarks</span></span>

<span data-ttu-id="7567a-112">La valeur de cette cellule correspond à la case à cocher **Demander lors de l’insertion** de la boîte de dialogue **Définir les données de forme** (cliquez avec le bouton droit sur la forme, pointez sur **Données**, puis cliquez sur **Définir les données de forme**).</span><span class="sxs-lookup"><span data-stu-id="7567a-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="7567a-113">Pour obtenir une référence à la cellule Ask par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7567a-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7567a-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="7567a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7567a-115">Hélice. *nom* . Vérifiez où prop.  *Name* est le nom de la ligne de propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7567a-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="7567a-116">Pour obtenir une référence référence à la cellule Ask à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7567a-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7567a-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7567a-117">Section index:</span></span>  <br/> |<span data-ttu-id="7567a-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="7567a-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="7567a-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7567a-119">Row index:</span></span>  <br/> |<span data-ttu-id="7567a-120">**visRowProp** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="7567a-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="7567a-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7567a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7567a-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="7567a-122">**visCustPropsAsk**</span></span> <br/> |
   

