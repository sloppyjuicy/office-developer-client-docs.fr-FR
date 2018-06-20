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
description: Exécute la chaîne et transmet les arguments de ligne de commande pour le programme sous forme de chaîne.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789585"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="8e776-103">RUNADDONWARGS, fonction</span><span class="sxs-lookup"><span data-stu-id="8e776-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="8e776-104">Exécute la _chaîne_ et transmet les _arguments_ ligne de commande pour le programme sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8e776-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8e776-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e776-105">Syntax</span></span>

<span data-ttu-id="8e776-106">RUNADDONWARGS (« ** *chaîne* ** », » ** *arguments* ** »)</span><span class="sxs-lookup"><span data-stu-id="8e776-106">RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8e776-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e776-107">Parameters</span></span>

|<span data-ttu-id="8e776-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e776-108">**Name**</span></span>|<span data-ttu-id="8e776-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8e776-109">**Required/Optional**</span></span>|<span data-ttu-id="8e776-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8e776-110">**Data Type**</span></span>|<span data-ttu-id="8e776-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8e776-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8e776-112">_string_</span><span class="sxs-lookup"><span data-stu-id="8e776-112">_string_</span></span> <br/> |<span data-ttu-id="8e776-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8e776-113">Required</span></span>  <br/> |<span data-ttu-id="8e776-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="8e776-114">**String**</span></span> <br/> | <span data-ttu-id="8e776-115">Nom d’un module complémentaire</span><span class="sxs-lookup"><span data-stu-id="8e776-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="8e776-116">_arguments_</span><span class="sxs-lookup"><span data-stu-id="8e776-116">_arguments_</span></span> <br/> |<span data-ttu-id="8e776-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8e776-117">Required</span></span>  <br/> |<span data-ttu-id="8e776-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="8e776-118">**String**</span></span> <br/> |<span data-ttu-id="8e776-119">Arguments à transmettre à votre programme</span><span class="sxs-lookup"><span data-stu-id="8e776-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e776-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e776-120">Remarks</span></span>

<span data-ttu-id="8e776-121">En pratique, _arguments_ doit comporter 50 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="8e776-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="8e776-122">Utilisez la fonction RUNADDONWARGS pour lier un programme, par exemple un module complémentaire, à une cellule, par exemple, à la cellule Action ou Events.</span><span class="sxs-lookup"><span data-stu-id="8e776-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="8e776-123">La fonction RUNADDONWARGS peut uniquement exécuter des modules complémentaires qui sont membres de la collection **Addons** de l’application.</span><span class="sxs-lookup"><span data-stu-id="8e776-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="8e776-124">Pour être présents dans la collection, un module complémentaire doit être un fichier EXE ou VSL qui est :</span><span class="sxs-lookup"><span data-stu-id="8e776-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="8e776-125">Installé dans le chemin d’accès **Startup** ou **Addons** de l’application.</span><span class="sxs-lookup"><span data-stu-id="8e776-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="8e776-126">Ajout par programme à l’aide de la méthode **Add** de la collection **Addons** .</span><span class="sxs-lookup"><span data-stu-id="8e776-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="8e776-127">Pour plus d’informations sur l’exécution de code dans Visio, voir [sur les paramètres de sécurité et l’exécution de Code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e776-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="8e776-p103">Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDONWARGS. Les versions de l’application Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.</span><span class="sxs-lookup"><span data-stu-id="8e776-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="8e776-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="8e776-130">Example</span></span>

<span data-ttu-id="8e776-131">RUNADDONWARGS (GRAPHMKR ». EXE », « / GraphMaker = Stack »)</span><span class="sxs-lookup"><span data-stu-id="8e776-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="8e776-132">Lance le module complémentaire Graphmkr.exe et lui transmet l’argument /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="8e776-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

