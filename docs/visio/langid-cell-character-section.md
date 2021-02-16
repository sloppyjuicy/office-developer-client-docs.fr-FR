---
title: LangID, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Indique la langue dans laquelle le texte a été entré.
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419281"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="20256-103">LangID, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="20256-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="20256-104">Indique la langue dans laquelle le texte a été entré.</span><span class="sxs-lookup"><span data-stu-id="20256-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20256-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="20256-105">Remarks</span></span>

<span data-ttu-id="20256-106">Pour une liste des langues prises en charge par les applications Microsoft Office, reportez-vous à la rubrique [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties).</span><span class="sxs-lookup"><span data-stu-id="20256-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="20256-107">Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="20256-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20256-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="20256-108">Cell name:</span></span>  <br/> | <span data-ttu-id="20256-109">Char.LangID[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="20256-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="20256-110">Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="20256-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20256-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="20256-111">Section index:</span></span>  <br/> |<span data-ttu-id="20256-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="20256-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="20256-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="20256-113">Row index:</span></span>  <br/> |<span data-ttu-id="20256-114">**visRowCharacter**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="20256-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="20256-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="20256-115">Cell index:</span></span>  <br/> |<span data-ttu-id="20256-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="20256-116">**visCharacterLangID**</span></span> <br/> |
   

