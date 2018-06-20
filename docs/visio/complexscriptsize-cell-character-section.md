---
title: ComplexScriptSize, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe.
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788308"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="6650e-103">ComplexScriptSize, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="6650e-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="6650e-104">Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe.</span><span class="sxs-lookup"><span data-stu-id="6650e-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6650e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="6650e-105">Remarks</span></span>

<span data-ttu-id="6650e-106">Tailles de police des scripts complexes sont répertoriés sous l’onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans la **police** de groupe sous l’onglet **accueil** ).</span><span class="sxs-lookup"><span data-stu-id="6650e-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="6650e-107">Cette liste apparaît uniquement si vous avez ajouté une langue qui contienne des caractères asiatiques ou à script complexe, dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="6650e-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="6650e-108">(Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="6650e-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="6650e-p102">Vous pouvez entrer cette valeur comme taille de point explicite ou comme pourcentage. Si vous indiquez un pourcentage, la valeur est basée sur celle de la cellule Size. Une valeur par défaut de 0 (zéro) signifie 100 %.</span><span class="sxs-lookup"><span data-stu-id="6650e-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="6650e-112">Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="6650e-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6650e-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6650e-113">Cell name:</span></span>  <br/> |<span data-ttu-id="6650e-114">Char.ComplexScriptSize [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6650e-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6650e-115">Pour obtenir une référence à la cellule ComplexScriptSize par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6650e-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6650e-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6650e-116">Section index:</span></span>  <br/> |<span data-ttu-id="6650e-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="6650e-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="6650e-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6650e-118">Row index:</span></span>  <br/> |<span data-ttu-id="6650e-119">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6650e-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6650e-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6650e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6650e-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="6650e-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

