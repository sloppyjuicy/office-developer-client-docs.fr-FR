---
title: ComplexScriptFont, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système.
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788303"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="a4bb7-104">ComplexScriptFont, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="a4bb7-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="a4bb7-p102">Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système.</span><span class="sxs-lookup"><span data-stu-id="a4bb7-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a4bb7-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4bb7-107">Remarks</span></span>

<span data-ttu-id="a4bb7-108">Tailles de police des scripts complexes sont répertoriés sous l’onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans la **police** de groupe sous l’onglet **accueil** ).</span><span class="sxs-lookup"><span data-stu-id="a4bb7-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="a4bb7-109">Cette liste apparaît uniquement si vous avez ajouté une langue qui contienne des caractères asiatiques ou à script complexe, dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="a4bb7-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="a4bb7-110">(Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="a4bb7-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="a4bb7-111">Le nombre 0 (zéro) signifie qu’aucune police n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a4bb7-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="a4bb7-112">La police Latin ou les polices par défaut sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="a4bb7-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="a4bb7-113">Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="a4bb7-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4bb7-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a4bb7-114">Cell name:</span></span>  <br/> |<span data-ttu-id="a4bb7-115">Char.ComplexScriptFont [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a4bb7-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a4bb7-116">Pour obtenir une référence à la cellule ComplexScriptFont par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4bb7-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4bb7-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a4bb7-117">Section index:</span></span>  <br/> |<span data-ttu-id="a4bb7-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a4bb7-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="a4bb7-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a4bb7-119">Row index:</span></span>  <br/> |<span data-ttu-id="a4bb7-120">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a4bb7-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a4bb7-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a4bb7-121">Cell index:</span></span>  <br/> |<span data-ttu-id="a4bb7-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="a4bb7-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

