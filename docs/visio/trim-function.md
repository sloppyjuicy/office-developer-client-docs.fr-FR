---
title: TRIM, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Supprime tout l'espace du texte, à l'exception des espaces simples entre les mots.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280842"
---
# <a name="trim-function"></a><span data-ttu-id="ec51e-103">Fonction TRIM</span><span class="sxs-lookup"><span data-stu-id="ec51e-103">TRIM Function</span></span>

<span data-ttu-id="ec51e-104">Supprime tout l'espace du texte, à l'exception des espaces simples entre les mots.</span><span class="sxs-lookup"><span data-stu-id="ec51e-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ec51e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec51e-105">Syntax</span></span>

<span data-ttu-id="ec51e-106">TRIM (\* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ec51e-106">TRIM (\*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ec51e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec51e-107">Parameters</span></span>

|<span data-ttu-id="ec51e-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ec51e-108">**Name**</span></span>|<span data-ttu-id="ec51e-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ec51e-109">**Required/Optional**</span></span>|<span data-ttu-id="ec51e-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ec51e-110">**Data Type**</span></span>|<span data-ttu-id="ec51e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec51e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ec51e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="ec51e-112">_text_</span></span> <br/> |<span data-ttu-id="ec51e-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ec51e-113">Required</span></span>  <br/> |<span data-ttu-id="ec51e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ec51e-114">**String**</span></span> <br/> |<span data-ttu-id="ec51e-115">Texte dont vous souhaitez supprimer les espaces.</span><span class="sxs-lookup"><span data-stu-id="ec51e-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ec51e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec51e-116">Return value</span></span>

<span data-ttu-id="ec51e-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ec51e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec51e-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec51e-118">Remarks</span></span>

<span data-ttu-id="ec51e-119">Vous pouvez utiliser la fonction TRIM sur du texte provenant d’une autre application qui utilise un espacement irrégulier.</span><span class="sxs-lookup"><span data-stu-id="ec51e-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="ec51e-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec51e-120">Example</span></span>

<span data-ttu-id="ec51e-121">TRIM ("janvier 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="ec51e-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="ec51e-122">Renvoie "2 janvier 2003".</span><span class="sxs-lookup"><span data-stu-id="ec51e-122">Returns "January 1, 2003".</span></span> 
  

