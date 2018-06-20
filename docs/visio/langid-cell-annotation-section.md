---
title: LangID, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indique la langue dans laquelle le commentaire a été entré.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788901"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="dd9a9-103">LangID, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="dd9a9-104">Indique la langue dans laquelle le commentaire a été entré.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dd9a9-105">Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="dd9a9-106">Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dd9a9-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd9a9-107">Remarks</span></span>

<span data-ttu-id="dd9a9-108">Cette valeur est le paramètre régional ID (LCID) de la langue qui est active dans la barre de langue lorsque le commentaire a été entré.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-108">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered.</span></span> <span data-ttu-id="dd9a9-109">Pour obtenir la liste des langues prises en charge par les applications Microsoft Office, consultez la rubrique de la cellule (Section Document Properties) [DocLangID](doclangid-cell-document-properties-section.md) .</span><span class="sxs-lookup"><span data-stu-id="dd9a9-109">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="dd9a9-110">Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="dd9a9-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd9a9-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd9a9-111">Cell name:</span></span>  <br/> | <span data-ttu-id="dd9a9-112">Annotation.LangID [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dd9a9-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dd9a9-113">Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dd9a9-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd9a9-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dd9a9-114">Section index:</span></span>  <br/> |<span data-ttu-id="dd9a9-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="dd9a9-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dd9a9-116">Row index:</span></span>  <br/> |<span data-ttu-id="dd9a9-117">**visRowAnnotation** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dd9a9-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dd9a9-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd9a9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="dd9a9-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-119">**visAnnotationLangID**</span></span> <br/> |
   

