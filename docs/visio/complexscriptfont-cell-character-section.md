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
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404833"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="66776-104">ComplexScriptFont, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="66776-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="66776-p102">Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système.</span><span class="sxs-lookup"><span data-stu-id="66776-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="66776-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="66776-107">Remarks</span></span>

<span data-ttu-id="66776-108">Les tailles de police de script complexe sont répertoriées sous l'onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans le groupe **police** de l'onglet **Accueil** ).</span><span class="sxs-lookup"><span data-stu-id="66776-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="66776-109">Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="66776-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="66776-110">(Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="66776-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="66776-111">Le numéro 0 (zéro) signifie qu'aucune police n'est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="66776-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="66776-112">La police Latin ou les polices par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="66776-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="66776-113">Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="66776-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66776-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="66776-114">Cell name:</span></span>  <br/> |<span data-ttu-id="66776-115">Char. ComplexScriptFont [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="66776-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="66776-116">Pour obtenir une référence à la cellule ComplexScriptFont à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="66776-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66776-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="66776-117">Section index:</span></span>  <br/> |<span data-ttu-id="66776-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="66776-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="66776-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="66776-119">Row index:</span></span>  <br/> |<span data-ttu-id="66776-120">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="66776-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="66776-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="66776-121">Cell index:</span></span>  <br/> |<span data-ttu-id="66776-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="66776-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

