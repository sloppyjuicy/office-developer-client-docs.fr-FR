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
ms.openlocfilehash: c5a0cca5f71bc5520337ad2bdcf354a2b4affe92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359030"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="0e938-103">LangID, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="0e938-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="0e938-104">Indique la langue dans laquelle les données forme ont été entrées.</span><span class="sxs-lookup"><span data-stu-id="0e938-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0e938-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e938-105">Remarks</span></span>

<span data-ttu-id="0e938-106">Pour une liste des langues prises en charge par les applications du système Microsoft Office, reportez-vous à la cellule [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties).</span><span class="sxs-lookup"><span data-stu-id="0e938-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="0e938-107">Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="0e938-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e938-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0e938-108">Cell name:</span></span>  <br/> | <span data-ttu-id="0e938-109">Hélice.  *nom* . ID de langue où prop.  *Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="0e938-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="0e938-110">Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0e938-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e938-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0e938-111">Section index:</span></span>  <br/> |<span data-ttu-id="0e938-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="0e938-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="0e938-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0e938-113">Row index:</span></span>  <br/> |<span data-ttu-id="0e938-114">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0e938-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0e938-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0e938-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0e938-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="0e938-116">**visCustPropsLangID**</span></span> <br/> |
   

