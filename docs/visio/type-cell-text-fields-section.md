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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407983"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="dab04-103">Type, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="dab04-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="dab04-104">Indique un type de données pour la valeur du champ de texte.</span><span class="sxs-lookup"><span data-stu-id="dab04-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="dab04-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dab04-105">**Value**</span></span>|<span data-ttu-id="dab04-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="dab04-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dab04-107">0</span><span class="sxs-lookup"><span data-stu-id="dab04-107">0</span></span>  <br/> |<span data-ttu-id="dab04-108">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="dab04-108">String.</span></span>  <br/> |
|<span data-ttu-id="dab04-109">2</span><span class="sxs-lookup"><span data-stu-id="dab04-109">2</span></span>  <br/> |<span data-ttu-id="dab04-p101">Nombre. Inclut les valeurs de date, d'heure, de durée ainsi que les valeurs monétaires, les échelles, les cotes et les angles. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="dab04-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="dab04-113">5 </span><span class="sxs-lookup"><span data-stu-id="dab04-113">5</span></span>  <br/> |<span data-ttu-id="dab04-p102">Valeur de date ou d'heure. Affiche les jours, les mois et les années ou les secondes, les minutes et les heures ou encore une date et une heure en même temps. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="dab04-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="dab04-117">6 </span><span class="sxs-lookup"><span data-stu-id="dab04-117">6</span></span>  <br/> |<span data-ttu-id="dab04-p103">Valeur de durée. Affiche le temps écoulé. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="dab04-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="dab04-121">7 </span><span class="sxs-lookup"><span data-stu-id="dab04-121">7</span></span>  <br/> |<span data-ttu-id="dab04-p104">Valeur monétaire. Utilise les paramètres régionaux actuels de votre système d'exploitation. Entrez un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="dab04-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dab04-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="dab04-125">Remarks</span></span>

<span data-ttu-id="dab04-126">Vous pouvez également définir la valeur de cette cellule à l’aide  de la  boîte de dialogue Champ (avec une forme sélectionnée, sous l’onglet Insertion, dans le groupe Texte, cliquez sur **Champ** ). </span><span class="sxs-lookup"><span data-stu-id="dab04-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="dab04-127">Pour obtenir une référence à la cellule Type par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="dab04-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab04-128">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="dab04-128">Cell name:</span></span>  <br/> |<span data-ttu-id="dab04-129">Fields.Type[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dab04-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dab04-130">Pour obtenir une référence à la cellule Type par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dab04-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab04-131">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dab04-131">Section index:</span></span>  <br/> |<span data-ttu-id="dab04-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="dab04-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="dab04-133">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dab04-133">Row index:</span></span>  <br/> |<span data-ttu-id="dab04-134">**visRowField**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dab04-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dab04-135">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dab04-135">Cell index:</span></span>  <br/> |<span data-ttu-id="dab04-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="dab04-136">**visFieldType**</span></span> <br/> |
   

