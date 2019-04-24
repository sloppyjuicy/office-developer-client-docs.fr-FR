---
title: HELP, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Ouvre un fichier d'aide HTML avec le mot clé spécifié dans la zone de recherche.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329973"
---
# <a name="help-function"></a><span data-ttu-id="d2892-103">Fonction HELP</span><span class="sxs-lookup"><span data-stu-id="d2892-103">HELP Function</span></span>

<span data-ttu-id="d2892-104">Ouvre un fichier d'aide HTML avec le *mot clé* spécifié dans la zone de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="d2892-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d2892-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2892-105">Syntax</span></span>

<span data-ttu-id="d2892-106">HELP ("\* \* *filename. chm! Keyword* \* \*")</span><span class="sxs-lookup"><span data-stu-id="d2892-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d2892-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2892-107">Parameters</span></span>

|<span data-ttu-id="d2892-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d2892-108">**Name**</span></span>|<span data-ttu-id="d2892-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d2892-109">**Required/Optional**</span></span>|<span data-ttu-id="d2892-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d2892-110">**Data Type**</span></span>|<span data-ttu-id="d2892-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2892-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d2892-112">_nom de fichier. chm! mot clé_</span><span class="sxs-lookup"><span data-stu-id="d2892-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="d2892-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d2892-113">Required</span></span>  <br/> |<span data-ttu-id="d2892-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d2892-114">**String**</span></span> <br/> | <span data-ttu-id="d2892-115">Nom du fichier d’aide et mot clé à rechercher.</span><span class="sxs-lookup"><span data-stu-id="d2892-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2892-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2892-116">Remarks</span></span>

<span data-ttu-id="d2892-117">Si aucun *mot clé* n'est spécifié, la fonction Help ouvre la page de contenu du fichier d'aide.</span><span class="sxs-lookup"><span data-stu-id="d2892-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d2892-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2892-118">Example</span></span>

<span data-ttu-id="d2892-119">HELP ("Visio. chm! ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="d2892-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="d2892-120">Ouvre le fichier d’aide Visio et affiche une liste de la ou des rubriques dont le mot clé est « shapesheet ».</span><span class="sxs-lookup"><span data-stu-id="d2892-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

