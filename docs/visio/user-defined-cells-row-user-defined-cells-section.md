---
title: User-defined Cells, ligne (section User-defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Contient la valeur et le message descriptif de toutes les cellules définies par l'utilisateur de votre solution. Une forme contient une ligne User-defined Cells pour chaque paire de cellules Value/Prompt.
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420688"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a><span data-ttu-id="25c04-104">User-defined Cells Row (User-defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="25c04-104">User-defined Cells Row (User-defined Cells Section)</span></span>

<span data-ttu-id="25c04-p102">Contient la valeur et le message descriptif de toutes les cellules définies par l'utilisateur de votre solution. Une forme contient une ligne User-defined Cells pour chaque paire de cellules Value/Prompt.</span><span class="sxs-lookup"><span data-stu-id="25c04-p102">Contains the value and descriptive prompt for any user-defined cells in your solution. A shape contains one User-defined Cells row for each user-defined Value/Prompt cell pair.</span></span>
  
<span data-ttu-id="25c04-107">Les lignes User-defined Cells sont nommées User.</span><span class="sxs-lookup"><span data-stu-id="25c04-107">User-defined Cells rows are named User.</span></span> <span data-ttu-id="25c04-108">*et*  contiennent les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="25c04-108">*name*  and contain the following cells.</span></span> <span data-ttu-id="25c04-109">Pour plus de détails, consultez les rubriques spécifiques aux cellules.</span><span class="sxs-lookup"><span data-stu-id="25c04-109">For more details, see the specific cell topics.</span></span> 
  
|<span data-ttu-id="25c04-110">**Cell**</span><span class="sxs-lookup"><span data-stu-id="25c04-110">**Cell**</span></span>|<span data-ttu-id="25c04-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="25c04-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25c04-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="25c04-112">Value</span></span>](value-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="25c04-113">Indique une valeur pour la cellule définie par l'utilisateur correspondante.</span><span class="sxs-lookup"><span data-stu-id="25c04-113">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |
|[<span data-ttu-id="25c04-114">Prompt</span><span class="sxs-lookup"><span data-stu-id="25c04-114">Prompt</span></span>](prompt-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="25c04-115">Indique un message descriptif ou commentaire pour la cellule définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="25c04-115">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c04-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="25c04-116">Remarks</span></span>

<span data-ttu-id="25c04-p104">Les cellules définies par l'utilisateur servent à entrer des formules ou constantes auxquelles d'autres cellules ou modules complémentaires font référence. Les valeurs des cellules définies par l'utilisateur sont portables. Cela signifie que, si une forme qui fait référence à une cellule définie par l'utilisateur dans une forme est copiée dans une autre forme ne possédant pas la même cellule définie par l'utilisateur, la cellule est ajoutée à la forme.</span><span class="sxs-lookup"><span data-stu-id="25c04-p104">User-defined cells can be used for entering formulas or constants that are referred to by other cells or add-ons. Values in user-defined cells are portable, that is, if a shape that refers to a user-defined cell in one shape is copied to another shape that does not have the same user-defined cell, the cell is added to the shape.</span></span>
  
 <span data-ttu-id="25c04-119">Vous pouvez ajouter autant de lignes User.</span><span class="sxs-lookup"><span data-stu-id="25c04-119">You can add as many User.</span></span>  <span data-ttu-id="25c04-120">*nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule.</span><span class="sxs-lookup"><span data-stu-id="25c04-120">*name*  rows as you need, assign meaningful names to the rows, and set cell values.</span></span> <span data-ttu-id="25c04-121">Pour ajouter une ligne à une section User-defined Cells existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="25c04-121">To add a row to an existing User-defined Cells section, right-click a row and click **Insert Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="25c04-122">Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="25c04-122">You can reference these cells by their row name, which appears in a ShapeSheet window in red text.</span></span> <span data-ttu-id="25c04-123">Pour assigner des noms parlants aux lignes User.</span><span class="sxs-lookup"><span data-stu-id="25c04-123">To assign meaningful names to User.</span></span> <span data-ttu-id="25c04-124">*name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset.</span><span class="sxs-lookup"><span data-stu-id="25c04-124">*name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset.</span></span> <span data-ttu-id="25c04-125">Vous pouvez alors faire référence à la cellule Prompt en utilisant User.Décalage.Prompt.</span><span class="sxs-lookup"><span data-stu-id="25c04-125">You can then reference the Prompt cell using User.Offset.Prompt.</span></span> 
  
<span data-ttu-id="25c04-126">Le nom de ligne que vous entrez doit être unique dans la section.</span><span class="sxs-lookup"><span data-stu-id="25c04-126">The row name you enter must be unique within the section.</span></span>
  

