---
title: OPENFILE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert et Active la fenêtre de document.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789188"
---
# <a name="openfile-function"></a><span data-ttu-id="9d728-103">OPENFILE, fonction</span><span class="sxs-lookup"><span data-stu-id="9d728-103">OPENFILE Function</span></span>

<span data-ttu-id="9d728-104">Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert et Active la fenêtre de document.</span><span class="sxs-lookup"><span data-stu-id="9d728-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9d728-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d728-105">Syntax</span></span>

 <span data-ttu-id="9d728-106">**OPENFILE** ( _« filename »_)</span><span class="sxs-lookup"><span data-stu-id="9d728-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="9d728-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d728-107">Parameters</span></span>

|<span data-ttu-id="9d728-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9d728-108">**Name**</span></span>|<span data-ttu-id="9d728-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9d728-109">**Required/Optional**</span></span>|<span data-ttu-id="9d728-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9d728-110">**Data Type**</span></span>|<span data-ttu-id="9d728-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d728-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9d728-112">_nom de fichier_</span><span class="sxs-lookup"><span data-stu-id="9d728-112">_filename_</span></span> <br/> |<span data-ttu-id="9d728-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9d728-113">Required</span></span>  <br/> |<span data-ttu-id="9d728-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d728-114">**String**</span></span> <br/> |<span data-ttu-id="9d728-115">Le nom du fichier, y compris le chemin d’accès du fichier, que vous souhaitez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="9d728-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d728-116">Note</span><span class="sxs-lookup"><span data-stu-id="9d728-116">Remarks</span></span>

<span data-ttu-id="9d728-p101">Si plusieurs fonctions OPENFILE sont déclenchées, elles sont mises en file d’attente et exécutées dans l’ordre d’évaluation. Si le document Visio ouvert est activé pour une modification à l’écran (dans une autre application), une nouvelle copie de Visio est lancée avec le nom de fichier demandé.</span><span class="sxs-lookup"><span data-stu-id="9d728-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="9d728-119">Cette fonction renvoie toujours la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d728-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="9d728-p102">Dans les versions précédentes de Visio, cette fonction s’appelait _OPENFILE. Les versions Visio 4.0 et ultérieures acceptent les deux styles.</span><span class="sxs-lookup"><span data-stu-id="9d728-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9d728-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d728-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="9d728-123">Ouvre le fichier « MyFile.vsdx » spécifié dans une nouvelle fenêtre ou Active la fenêtre si le fichier est déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="9d728-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

