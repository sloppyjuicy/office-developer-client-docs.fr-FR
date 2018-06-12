---
title: Format, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788687"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="2098f-103">Format, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="2098f-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="2098f-104">Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.</span><span class="sxs-lookup"><span data-stu-id="2098f-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2098f-105">Notes</span><span class="sxs-lookup"><span data-stu-id="2098f-105">Remarks</span></span>

<span data-ttu-id="2098f-106">Si la valeur de la cellule Type est 0, 2, 5, 6 ou 7 (chaîne, nombre, date ou heure, durée ou devise, respectivement), spécifiez un modèle de format approprié pour le type de données.</span><span class="sxs-lookup"><span data-stu-id="2098f-106">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type.</span></span> <span data-ttu-id="2098f-107">Par exemple, le modèle de format « # #/ 4 UU » met en forme les numéros de 12,43 ;.</span><span class="sxs-lookup"><span data-stu-id="2098f-107">For example, the format picture "# #/4 UU" formats the number 12.43 in.</span></span> <span data-ttu-id="2098f-108">en tant que 12 2/4 pouces.</span><span class="sxs-lookup"><span data-stu-id="2098f-108">as 12 2/4 INCHES.</span></span> <span data-ttu-id="2098f-109">Pour plus d’informations sur la spécification d’un format de l’image, voir [à propos des modèles de format](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="2098f-109">For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="2098f-p102">Un nombre (Type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre saisi est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.</span><span class="sxs-lookup"><span data-stu-id="2098f-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="2098f-112">Pour obtenir une référence à la cellule Format par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2098f-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2098f-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2098f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2098f-114">Fields.Format [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2098f-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2098f-115">Pour obtenir une référence à la cellule Format par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2098f-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2098f-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2098f-116">Section index:</span></span>  <br/> |<span data-ttu-id="2098f-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="2098f-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="2098f-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2098f-118">Row index:</span></span>  <br/> |<span data-ttu-id="2098f-119">**visRowField** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2098f-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2098f-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2098f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2098f-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="2098f-121">**visFieldFormat**</span></span> <br/> |
   

