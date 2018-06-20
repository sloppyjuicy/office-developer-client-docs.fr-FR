---
title: LangID, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indique la langue dans laquelle les données forme ont été entrées.
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788920"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="d2161-103">LangID, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="d2161-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="d2161-104">Indique la langue dans laquelle les données forme ont été entrées.</span><span class="sxs-lookup"><span data-stu-id="d2161-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2161-105">Notes</span><span class="sxs-lookup"><span data-stu-id="d2161-105">Remarks</span></span>

<span data-ttu-id="d2161-106">Pour obtenir la liste des langues prises en charge par les applications Microsoft Office System, reportez-vous à la cellule [DocLangID](doclangid-cell-document-properties-section.md) (Section Document Properties).</span><span class="sxs-lookup"><span data-stu-id="d2161-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="d2161-107">Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d2161-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2161-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2161-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d2161-109">Propriétés.  *nom* . LangID où de propriétés.  *Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="d2161-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d2161-110">Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d2161-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2161-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d2161-111">Section index:</span></span>  <br/> |<span data-ttu-id="d2161-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d2161-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d2161-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d2161-113">Row index:</span></span>  <br/> |<span data-ttu-id="d2161-114">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d2161-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d2161-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2161-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d2161-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="d2161-116">**visCustPropsLangID**</span></span> <br/> |
   

