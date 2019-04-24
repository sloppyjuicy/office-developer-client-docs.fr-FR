---
title: Type, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Indique un type de données pour la valeur du champ de texte.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358925"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="48f68-103">Type, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="48f68-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="48f68-104">Indique un type de données pour la valeur du champ de texte.</span><span class="sxs-lookup"><span data-stu-id="48f68-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="48f68-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="48f68-105">**Value**</span></span>|<span data-ttu-id="48f68-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="48f68-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48f68-107">0</span><span class="sxs-lookup"><span data-stu-id="48f68-107">0</span></span>  <br/> |<span data-ttu-id="48f68-108">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="48f68-108">String.</span></span>  <br/> |
|<span data-ttu-id="48f68-109">n°2</span><span class="sxs-lookup"><span data-stu-id="48f68-109">2</span></span>  <br/> |<span data-ttu-id="48f68-p101">Nombre. Inclut les valeurs de date, d'heure, de durée ainsi que les valeurs monétaires, les échelles, les cotes et les angles. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="48f68-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="48f68-113">disque</span><span class="sxs-lookup"><span data-stu-id="48f68-113">5</span></span>  <br/> |<span data-ttu-id="48f68-p102">Valeur de date ou d'heure. Affiche les jours, les mois et les années ou les secondes, les minutes et les heures ou encore une date et une heure en même temps. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="48f68-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="48f68-117">6.x</span><span class="sxs-lookup"><span data-stu-id="48f68-117">6</span></span>  <br/> |<span data-ttu-id="48f68-p103">Valeur de durée. Affiche le temps écoulé. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="48f68-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="48f68-121">7j/7</span><span class="sxs-lookup"><span data-stu-id="48f68-121">7</span></span>  <br/> |<span data-ttu-id="48f68-p104">Valeur monétaire. Utilise les paramètres régionaux actuels de votre système d'exploitation. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="48f68-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48f68-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="48f68-125">Remarks</span></span>

<span data-ttu-id="48f68-126">Vous pouvez également définir la valeur de cette cellule à l'aide de la boîte de dialogue **champ** (avec une forme sélectionnée, sous l'onglet **insertion** , dans le groupe **texte** , cliquez sur **champ** ).</span><span class="sxs-lookup"><span data-stu-id="48f68-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="48f68-127">Pour obtenir une référence à la cellule Type par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="48f68-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48f68-128">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="48f68-128">Cell name:</span></span>  <br/> |<span data-ttu-id="48f68-129">Fields. type [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="48f68-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="48f68-130">Pour obtenir une référence à la cellule Type par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="48f68-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48f68-131">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="48f68-131">Section index:</span></span>  <br/> |<span data-ttu-id="48f68-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="48f68-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="48f68-133">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="48f68-133">Row index:</span></span>  <br/> |<span data-ttu-id="48f68-134">**visRowField** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="48f68-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="48f68-135">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="48f68-135">Cell index:</span></span>  <br/> |<span data-ttu-id="48f68-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="48f68-136">**visFieldType**</span></span> <br/> |
   

