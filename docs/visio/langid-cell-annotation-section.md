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
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422256"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="dbc17-103">LangID, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="dbc17-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="dbc17-104">Indique la langue dans laquelle le commentaire a été entré.</span><span class="sxs-lookup"><span data-stu-id="dbc17-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dbc17-105">Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l'ouverture d'un fichier. VSD dans Microsoft Visio 2013 ou lors de l'enregistrement d'un fichier. vsdx au format de fichier. VSD.</span><span class="sxs-lookup"><span data-stu-id="dbc17-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="dbc17-106">Il n'est pas utilisé pour suivre les commentaires dans les documents. vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="dbc17-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dbc17-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="dbc17-107">Remarks</span></span>

<span data-ttu-id="dbc17-p102">Cette valeur est l’ID de paramètres régionaux (LCID) de la langue active dans la barre de langue lorsque le commentaire a été entré. Pour une liste des langues prises en charge par les applications Microsoft Office, reportez-vous à la rubrique [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties).</span><span class="sxs-lookup"><span data-stu-id="dbc17-p102">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered. For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="dbc17-110">Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="dbc17-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbc17-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dbc17-111">Cell name:</span></span>  <br/> | <span data-ttu-id="dbc17-112">Annotation. LangID [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dbc17-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dbc17-113">Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dbc17-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbc17-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dbc17-114">Section index:</span></span>  <br/> |<span data-ttu-id="dbc17-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="dbc17-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="dbc17-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dbc17-116">Row index:</span></span>  <br/> |<span data-ttu-id="dbc17-117">**visRowAnnotation** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dbc17-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dbc17-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dbc17-118">Cell index:</span></span>  <br/> |<span data-ttu-id="dbc17-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="dbc17-119">**visAnnotationLangID**</span></span> <br/> |
   

