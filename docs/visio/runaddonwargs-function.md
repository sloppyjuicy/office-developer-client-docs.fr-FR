---
title: RUNADDONWARGS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Exécute une chaîne et transmet les arguments de ligne de commande au programme en tant que chaîne.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408704"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="39763-103">Fonction RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="39763-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="39763-104">Exécute  _une_ chaîne et transmet les  _arguments_ de ligne de commande au programme en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="39763-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="39763-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39763-105">Syntax</span></span>

<span data-ttu-id="39763-106">RUNADDONWARGS( » \*\* *string* \*\* « , » \*\* *arguments* \*\* « )</span><span class="sxs-lookup"><span data-stu-id="39763-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="39763-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39763-107">Parameters</span></span>

|<span data-ttu-id="39763-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="39763-108">**Name**</span></span>|<span data-ttu-id="39763-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="39763-109">**Required/Optional**</span></span>|<span data-ttu-id="39763-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="39763-110">**Data Type**</span></span>|<span data-ttu-id="39763-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="39763-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="39763-112">_string_</span><span class="sxs-lookup"><span data-stu-id="39763-112">_string_</span></span> <br/> |<span data-ttu-id="39763-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="39763-113">Required</span></span>  <br/> |<span data-ttu-id="39763-114">**String**</span><span class="sxs-lookup"><span data-stu-id="39763-114">**String**</span></span> <br/> | <span data-ttu-id="39763-115">Nom d’un module complémentaire</span><span class="sxs-lookup"><span data-stu-id="39763-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="39763-116">_arguments_</span><span class="sxs-lookup"><span data-stu-id="39763-116">_arguments_</span></span> <br/> |<span data-ttu-id="39763-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="39763-117">Required</span></span>  <br/> |<span data-ttu-id="39763-118">**String**</span><span class="sxs-lookup"><span data-stu-id="39763-118">**String**</span></span> <br/> |<span data-ttu-id="39763-119">Arguments à transmettre à votre programme</span><span class="sxs-lookup"><span data-stu-id="39763-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39763-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="39763-120">Remarks</span></span>

<span data-ttu-id="39763-121">Dans la pratique,  _les arguments_ doivent être de 50 caractères ou moins.</span><span class="sxs-lookup"><span data-stu-id="39763-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="39763-122">Utilisez la fonction RUNADDONWARGS pour lier un programme, tel qu’un module complémentaire, à une cellule, par exemple à la cellule Action ou Events.</span><span class="sxs-lookup"><span data-stu-id="39763-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="39763-123">La fonction RUNADDONWARGS ne peut exécuter que des modules complémentaires membres de la collection **Addons** de l’application.</span><span class="sxs-lookup"><span data-stu-id="39763-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="39763-124">Pour faire partie de cette collection, un module complémentaire doit être un fichier EXE ou VSL qui est :</span><span class="sxs-lookup"><span data-stu-id="39763-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="39763-125">installé dans le chemin d’accès **Startup** ou **Addons** de l’application ;</span><span class="sxs-lookup"><span data-stu-id="39763-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="39763-126">ajouté par programme à l’aide de la méthode **Add** de la collection **Addons**.</span><span class="sxs-lookup"><span data-stu-id="39763-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="39763-127">Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="39763-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="39763-p103">Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDONWARGS. Les versions de l’application Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.</span><span class="sxs-lookup"><span data-stu-id="39763-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="39763-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="39763-130">Example</span></span>

<span data-ttu-id="39763-131">RUNADDONWARGS(« GRAPHMKR.EXE »,"/GraphMaker=Stack »)</span><span class="sxs-lookup"><span data-stu-id="39763-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="39763-132">Lance le module complémentaire Graphmkr.exe et lui transmet l’argument /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="39763-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

