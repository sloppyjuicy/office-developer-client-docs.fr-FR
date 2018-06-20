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
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788897"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="40413-103">LangID, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="40413-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="40413-104">Indique la langue dans laquelle le texte a été entré.</span><span class="sxs-lookup"><span data-stu-id="40413-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="40413-105">Notes</span><span class="sxs-lookup"><span data-stu-id="40413-105">Remarks</span></span>

<span data-ttu-id="40413-106">Pour obtenir la liste des langues prises en charge par les applications Microsoft Office, consultez la rubrique de la cellule (Section Document Properties) [DocLangID](doclangid-cell-document-properties-section.md) .</span><span class="sxs-lookup"><span data-stu-id="40413-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="40413-107">Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="40413-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40413-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40413-108">Cell name:</span></span>  <br/> | <span data-ttu-id="40413-109">Char.LangID [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="40413-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="40413-110">Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="40413-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40413-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="40413-111">Section index:</span></span>  <br/> |<span data-ttu-id="40413-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="40413-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="40413-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="40413-113">Row index:</span></span>  <br/> |<span data-ttu-id="40413-114">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="40413-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="40413-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40413-115">Cell index:</span></span>  <br/> |<span data-ttu-id="40413-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="40413-116">**visCharacterLangID**</span></span> <br/> |
   

