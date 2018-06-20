---
title: LangID, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Indique la langue dans laquelle les formules de la cellule ont été créées.
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788940"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="fc44a-103">LangID, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="fc44a-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fc44a-104">Indique la langue dans laquelle les formules de la cellule ont été créées.</span><span class="sxs-lookup"><span data-stu-id="fc44a-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fc44a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="fc44a-105">Remarks</span></span>

<span data-ttu-id="fc44a-106">Pour obtenir la liste des langues prises en charge par les applications Microsoft Office, consultez la rubrique de la cellule (Section Document Properties) [DocLangID](doclangid-cell-document-properties-section.md) .</span><span class="sxs-lookup"><span data-stu-id="fc44a-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="fc44a-107">Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fc44a-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc44a-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fc44a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="fc44a-109">ID de langue</span><span class="sxs-lookup"><span data-stu-id="fc44a-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="fc44a-110">Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fc44a-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc44a-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fc44a-111">Section index:</span></span>  <br/> |<span data-ttu-id="fc44a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fc44a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fc44a-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fc44a-113">Row index:</span></span>  <br/> |<span data-ttu-id="fc44a-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="fc44a-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="fc44a-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fc44a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="fc44a-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="fc44a-116">**visObjLangID**</span></span> <br/> |
   

