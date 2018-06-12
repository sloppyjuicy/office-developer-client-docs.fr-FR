---
title: FIELDPICTURE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Renvoie une chaîne de format de l’image qui établit une correspondance avec le code de format de champ de texte interne Microsoft Visio.
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788597"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="6e7c3-103">FIELDPICTURE, fonction</span><span class="sxs-lookup"><span data-stu-id="6e7c3-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="6e7c3-104">Renvoie une chaîne de format de l’image qui établit une correspondance avec le code de format de champ de texte interne Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6e7c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e7c3-105">Syntax</span></span>

<span data-ttu-id="6e7c3-106">FIELDPICTURE (** *code* **)</span><span class="sxs-lookup"><span data-stu-id="6e7c3-106">FIELDPICTURE(** *code* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e7c3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e7c3-107">Parameters</span></span>

|<span data-ttu-id="6e7c3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e7c3-108">**Name**</span></span>|<span data-ttu-id="6e7c3-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="6e7c3-109">**Required/Optional**</span></span>|<span data-ttu-id="6e7c3-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="6e7c3-110">**Data Type**</span></span>|<span data-ttu-id="6e7c3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="6e7c3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e7c3-112">_code_</span><span class="sxs-lookup"><span data-stu-id="6e7c3-112">_code_</span></span> <br/> |<span data-ttu-id="6e7c3-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6e7c3-113">Required</span></span>  <br/> |<span data-ttu-id="6e7c3-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="6e7c3-114">**Number**</span></span> <br/> | <span data-ttu-id="6e7c3-115">Code de format de champ de texte.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6e7c3-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6e7c3-116">Return value</span></span>

<span data-ttu-id="6e7c3-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="6e7c3-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e7c3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e7c3-118">Remarks</span></span>

<span data-ttu-id="6e7c3-119">Les chaînes de modèle de format sont utilisées par la fonction FORMAT pour définir le développement des valeurs en dates, heures, nombres et intitulés d’unité.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="6e7c3-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="6e7c3-120">Example</span></span>

<span data-ttu-id="6e7c3-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="6e7c3-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="6e7c3-122">Renvoie la chaîne de modèle de format « esc(0) », qui permet de représenter un nombre à une décimale dont l’unité est en minuscule lorsque la fonction FORMAT est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

