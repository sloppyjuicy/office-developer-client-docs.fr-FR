---
title: SubAddress, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Indique un emplacement au sein du document cible vers lequel établir un lien.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349321"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="21329-103">SubAddress, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="21329-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="21329-104">Indique un emplacement au sein du document cible vers lequel établir un lien.</span><span class="sxs-lookup"><span data-stu-id="21329-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21329-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="21329-105">Remarks</span></span>

<span data-ttu-id="21329-106">Par exemple, si la cellule Address est "drawing1. vsdx", la cellule subAddress peut spécifier un nom de page tel que "page-3".</span><span class="sxs-lookup"><span data-stu-id="21329-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="21329-107">Si la cellule Address est le fichier Microsoft Excel "Samples. xlsx", la valeur de cette cellule peut être une feuille de calcul ou une plage dans une feuille de calcul, telle que «fonctions de feuille de calcul» ou «Sheet1! A1: D10 ".</span><span class="sxs-lookup"><span data-stu-id="21329-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="21329-108">Si la cellule Address est «https://www.microsoft.com/office/», la valeur de cette cellule peut être une ancre nommée dans le document, telle que «solutions».</span><span class="sxs-lookup"><span data-stu-id="21329-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="21329-109">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Liens hypertexte** (dans le groupe **Liens** sous l’onglet **Insertion**, cliquez sur **Lien hypertexte**).</span><span class="sxs-lookup"><span data-stu-id="21329-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="21329-110">Pour obtenir une référence à la cellule SubAddress à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="21329-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21329-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="21329-111">Cell name:</span></span>  <br/> | <span data-ttu-id="21329-112">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="21329-112">Hyperlink.</span></span>  <span data-ttu-id="21329-113">*nom* . SubAddress, où hyperLink *. nom* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="21329-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="21329-114">Pour obtenir une référence à la \*\*\*\* cellule SubAddress à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="21329-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21329-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="21329-115">Section index:</span></span>  <br/> |<span data-ttu-id="21329-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="21329-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="21329-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="21329-117">Row index:</span></span>  <br/> |<span data-ttu-id="21329-118">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="21329-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="21329-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="21329-119">Cell index:</span></span>  <br/> |<span data-ttu-id="21329-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="21329-120">**visHLinkSubAddress**</span></span> <br/> |
   

