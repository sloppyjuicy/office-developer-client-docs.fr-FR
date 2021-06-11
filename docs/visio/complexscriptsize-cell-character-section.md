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
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428437"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="d87b9-103">ComplexScriptSize, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="d87b9-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="d87b9-104">Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe.</span><span class="sxs-lookup"><span data-stu-id="d87b9-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d87b9-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d87b9-105">Remarks</span></span>

<span data-ttu-id="d87b9-106">Les tailles de police de script  complexes sont répertoriées sous  l’onglet Police de la boîte de dialogue Texte (cliquez sur la flèche du groupe Police sous **l’onglet Accueil).** </span><span class="sxs-lookup"><span data-stu-id="d87b9-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="d87b9-107">Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="d87b9-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="d87b9-108">(Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="d87b9-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="d87b9-p102">Vous pouvez entrer cette valeur comme taille de point explicite ou comme pourcentage. Si vous indiquez un pourcentage, la valeur est basée sur celle de la cellule Size. Une valeur par défaut de 0 (zéro) signifie 100 %.</span><span class="sxs-lookup"><span data-stu-id="d87b9-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="d87b9-112">Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d87b9-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d87b9-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d87b9-113">Cell name:</span></span>  <br/> |<span data-ttu-id="d87b9-114">Char.ComplexScriptSize[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d87b9-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d87b9-115">Pour obtenir une référence à la cellule ComplexScriptSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d87b9-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d87b9-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d87b9-116">Section index:</span></span>  <br/> |<span data-ttu-id="d87b9-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d87b9-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d87b9-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d87b9-118">Row index:</span></span>  <br/> |<span data-ttu-id="d87b9-119">**visRowCharacter**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d87b9-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d87b9-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d87b9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d87b9-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="d87b9-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

