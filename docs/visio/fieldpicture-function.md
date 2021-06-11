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
description: Renvoie une chaîne d’image de format qui correspond au code de format Visio de champ de texte interne Microsoft.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431455"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="80298-103">Fonction FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="80298-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="80298-104">Renvoie une chaîne d’image de format qui correspond au code de format Visio de champ de texte interne Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80298-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="80298-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80298-105">Syntax</span></span>

<span data-ttu-id="80298-106">FIELDPICTURE(\*\* *code* \*\* )</span><span class="sxs-lookup"><span data-stu-id="80298-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="80298-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80298-107">Parameters</span></span>

|<span data-ttu-id="80298-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="80298-108">**Name**</span></span>|<span data-ttu-id="80298-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="80298-109">**Required/Optional**</span></span>|<span data-ttu-id="80298-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="80298-110">**Data Type**</span></span>|<span data-ttu-id="80298-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="80298-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="80298-112">_code_</span><span class="sxs-lookup"><span data-stu-id="80298-112">_code_</span></span> <br/> |<span data-ttu-id="80298-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="80298-113">Required</span></span>  <br/> |<span data-ttu-id="80298-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="80298-114">**Number**</span></span> <br/> | <span data-ttu-id="80298-115">Code de format de champ de texte.</span><span class="sxs-lookup"><span data-stu-id="80298-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="80298-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="80298-116">Return value</span></span>

<span data-ttu-id="80298-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="80298-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80298-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="80298-118">Remarks</span></span>

<span data-ttu-id="80298-119">Les chaînes de modèle de format sont utilisées par la fonction FORMAT pour définir le développement des valeurs en dates, heures, nombres et intitulés d’unité.</span><span class="sxs-lookup"><span data-stu-id="80298-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="80298-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="80298-120">Example</span></span>

<span data-ttu-id="80298-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="80298-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="80298-122">Renvoie la chaîne de modèle de format « esc(0) », qui permet de représenter un nombre à une décimale dont l’unité est en minuscule lorsque la fonction FORMAT est utilisée.</span><span class="sxs-lookup"><span data-stu-id="80298-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

