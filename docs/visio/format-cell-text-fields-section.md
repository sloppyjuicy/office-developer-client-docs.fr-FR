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
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431518"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="87557-103">Format, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="87557-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="87557-104">Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.</span><span class="sxs-lookup"><span data-stu-id="87557-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87557-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="87557-105">Remarks</span></span>

<span data-ttu-id="87557-p101">Si la valeur de la cellule Type est 0, 2, 5, 6 ou 7 (respectivement une chaîne, un nombre, une date ou une heure, une durée ou une devise), indiquez un type de format approprié pour le type de données. Par exemple, le modèle de format « # #/4 UU » fait apparaître le nombre 315,7 mm sous la forme 315 3/4 MILLIMÈTRES. Pour plus d'informations sur la saisie d'un modèle de format, reportez-vous à [À propos des modèles de format](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="87557-p101">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type. For example, the format picture "# #/4 UU" formats the number 12.43 in. as 12 2/4 INCHES. For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="87557-p102">Un nombre (Type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre saisi est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.</span><span class="sxs-lookup"><span data-stu-id="87557-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="87557-112">Pour obtenir une référence à la cellule Format par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="87557-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87557-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="87557-113">Cell name:</span></span>  <br/> | <span data-ttu-id="87557-114">Fields.Format[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="87557-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="87557-115">Pour obtenir une référence à la cellule Format à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="87557-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87557-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="87557-116">Section index:</span></span>  <br/> |<span data-ttu-id="87557-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="87557-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="87557-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="87557-118">Row index:</span></span>  <br/> |<span data-ttu-id="87557-119">**visRowField**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87557-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="87557-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="87557-120">Cell index:</span></span>  <br/> |<span data-ttu-id="87557-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="87557-121">**visFieldFormat**</span></span> <br/> |
   

