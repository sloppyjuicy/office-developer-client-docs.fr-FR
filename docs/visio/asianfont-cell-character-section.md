---
title: AsianFont, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contient le numéro de la police utilisée pour mettre en forme le texte comportant des caractères asiatiques. Les numéros de police varient en fonction des polices installées sur votre système.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788024"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="32b08-104">AsianFont, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="32b08-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="32b08-p102">Contient le numéro de la police utilisée pour mettre en forme le texte comportant des caractères asiatiques. Les numéros de police varient en fonction des polices installées sur votre système.</span><span class="sxs-lookup"><span data-stu-id="32b08-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32b08-107">Note</span><span class="sxs-lookup"><span data-stu-id="32b08-107">Remarks</span></span>

<span data-ttu-id="32b08-108">Les polices asiatiques sont répertoriées sous l’onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans la **police** de groupe sous l’onglet **accueil** ).</span><span class="sxs-lookup"><span data-stu-id="32b08-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="32b08-109">Cette liste apparaît uniquement si vous avez ajouté une langue qui contienne des caractères asiatiques ou à script complexe, dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="32b08-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="32b08-110">(Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="32b08-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="32b08-p104">Le numéro 0 signifie qu'aucune police n'est spécifiée. La police Latin ou les polices par défaut sont utilisées si elles contiennent les caractères nécessaires.</span><span class="sxs-lookup"><span data-stu-id="32b08-p104">The number 0 means no font is specified. The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="32b08-113">Pour obtenir une référence à la cellule AsianFont par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="32b08-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32b08-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="32b08-114">Cell name:</span></span>  <br/> |<span data-ttu-id="32b08-115">Char.AsianFont [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="32b08-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="32b08-116">Pour obtenir une référence à la cellule AsianFont par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="32b08-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32b08-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="32b08-117">Section index:</span></span>  <br/> |<span data-ttu-id="32b08-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="32b08-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="32b08-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="32b08-119">Row index:</span></span>  <br/> |<span data-ttu-id="32b08-120">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="32b08-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="32b08-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="32b08-121">Cell index:</span></span>  <br/> |<span data-ttu-id="32b08-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="32b08-122">**visCharacterAsianFont**</span></span> <br/> |
   

