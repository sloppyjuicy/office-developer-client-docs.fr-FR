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
description: Ouvre un fichier d’aide HTML avec le mot clé spécifié dans la zone de recherche.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788768"
---
# <a name="help-function"></a><span data-ttu-id="f7d50-103">HELP, fonction</span><span class="sxs-lookup"><span data-stu-id="f7d50-103">HELP Function</span></span>

<span data-ttu-id="f7d50-104">Ouvre un fichier d’aide HTML avec le *mot clé* de spécifié dans la zone de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="f7d50-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f7d50-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7d50-105">Syntax</span></span>

<span data-ttu-id="f7d50-106">AIDE (« ** *nomfichier.chm ! mot clé* ** »)</span><span class="sxs-lookup"><span data-stu-id="f7d50-106">HELP(" ** *filename.chm!keyword* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f7d50-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7d50-107">Parameters</span></span>

|<span data-ttu-id="f7d50-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f7d50-108">**Name**</span></span>|<span data-ttu-id="f7d50-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f7d50-109">**Required/Optional**</span></span>|<span data-ttu-id="f7d50-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f7d50-110">**Data Type**</span></span>|<span data-ttu-id="f7d50-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f7d50-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f7d50-112">_nomfichier.chm ! mot clé_</span><span class="sxs-lookup"><span data-stu-id="f7d50-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="f7d50-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7d50-113">Required</span></span>  <br/> |<span data-ttu-id="f7d50-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7d50-114">**String**</span></span> <br/> | <span data-ttu-id="f7d50-115">Nom du fichier d’aide et mot clé à rechercher.</span><span class="sxs-lookup"><span data-stu-id="f7d50-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7d50-116">Note</span><span class="sxs-lookup"><span data-stu-id="f7d50-116">Remarks</span></span>

<span data-ttu-id="f7d50-117">Si aucun *mot clé* n’est spécifié, la fonction HELP ouvre la page contenu du fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="f7d50-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f7d50-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7d50-118">Example</span></span>

<span data-ttu-id="f7d50-119">Help("Visio.chm!ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="f7d50-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="f7d50-120">Ouvre le fichier d’aide Visio et affiche une liste de la ou des rubriques dont le mot clé est « shapesheet ».</span><span class="sxs-lookup"><span data-stu-id="f7d50-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

