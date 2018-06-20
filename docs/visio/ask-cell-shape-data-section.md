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
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788016"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="05ddb-103">Ask, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="05ddb-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="05ddb-104">Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.</span><span class="sxs-lookup"><span data-stu-id="05ddb-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="05ddb-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="05ddb-105">**Value**</span></span>|<span data-ttu-id="05ddb-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="05ddb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05ddb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="05ddb-107">TRUE</span></span>  <br/> |<span data-ttu-id="05ddb-108">Demandez à l’utilisateur à entrer des données de forme dans la boîte de dialogue **Définir les données de forme** .</span><span class="sxs-lookup"><span data-stu-id="05ddb-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="05ddb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="05ddb-109">FALSE</span></span>  <br/> |<span data-ttu-id="05ddb-110">N’est pas invité à entrer des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05ddb-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05ddb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="05ddb-111">Remarks</span></span>

<span data-ttu-id="05ddb-112">La valeur de cette cellule correspond à la case à cocher **Demander lors de l’insertion** dans la boîte de dialogue **Définir les données de forme** (avec le bouton droit de la forme, pointez sur **données**, puis cliquez sur **Définir les données de forme**).</span><span class="sxs-lookup"><span data-stu-id="05ddb-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="05ddb-113">Pour obtenir une référence à la cellule Ask par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="05ddb-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05ddb-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="05ddb-114">Cell name:</span></span>  <br/> |<span data-ttu-id="05ddb-115">Propriétés. *nom* . Vérifiez où de propriétés.  *nom* est le nom de la ligne de propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="05ddb-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="05ddb-116">Pour obtenir une référence à la cellule Ask par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="05ddb-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05ddb-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="05ddb-117">Section index:</span></span>  <br/> |<span data-ttu-id="05ddb-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="05ddb-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="05ddb-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="05ddb-119">Row index:</span></span>  <br/> |<span data-ttu-id="05ddb-120">**visRowProp** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="05ddb-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="05ddb-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="05ddb-121">Cell index:</span></span>  <br/> |<span data-ttu-id="05ddb-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="05ddb-122">**visCustPropsAsk**</span></span> <br/> |
   

