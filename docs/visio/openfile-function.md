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
description: Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert, et active la fenêtre de document.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419575"
---
# <a name="openfile-function"></a><span data-ttu-id="76656-103">Fonction OPENFILE</span><span class="sxs-lookup"><span data-stu-id="76656-103">OPENFILE Function</span></span>

<span data-ttu-id="76656-104">Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert, et active la fenêtre de document.</span><span class="sxs-lookup"><span data-stu-id="76656-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="76656-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76656-105">Syntax</span></span>

 <span data-ttu-id="76656-106">**OPENFILE**( _« filename »_)</span><span class="sxs-lookup"><span data-stu-id="76656-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="76656-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76656-107">Parameters</span></span>

|<span data-ttu-id="76656-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="76656-108">**Name**</span></span>|<span data-ttu-id="76656-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="76656-109">**Required/Optional**</span></span>|<span data-ttu-id="76656-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="76656-110">**Data Type**</span></span>|<span data-ttu-id="76656-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="76656-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76656-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="76656-112">_filename_</span></span> <br/> |<span data-ttu-id="76656-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="76656-113">Required</span></span>  <br/> |<span data-ttu-id="76656-114">**String**</span><span class="sxs-lookup"><span data-stu-id="76656-114">**String**</span></span> <br/> |<span data-ttu-id="76656-115">Nom du fichier, y compris le chemin d’accès au fichier, que vous souhaitez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="76656-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76656-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="76656-116">Remarks</span></span>

<span data-ttu-id="76656-p101">Si plusieurs fonctions OPENFILE sont déclenchées, elles sont mises en file d’attente et exécutées dans l’ordre d’évaluation. Si le document Visio ouvert est activé pour une modification à l’écran (dans une autre application), une nouvelle copie de Visio est lancée avec le nom de fichier demandé.</span><span class="sxs-lookup"><span data-stu-id="76656-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="76656-119">Cette fonction renvoie toujours la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="76656-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="76656-p102">Dans les versions précédentes de Visio, cette fonction s’appelait _OPENFILE. Les versions Visio 4.0 et ultérieures acceptent les deux styles.</span><span class="sxs-lookup"><span data-stu-id="76656-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="76656-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="76656-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="76656-123">Ouvre le fichier spécifié « MyFile.vsdx » dans une nouvelle fenêtre ou active la fenêtre si le fichier est déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="76656-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

