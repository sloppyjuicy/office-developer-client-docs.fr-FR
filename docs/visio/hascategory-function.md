---
title: HASCATEGORY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433352"
---
# <a name="hascategory-function"></a><span data-ttu-id="9cf16-103">Fonction HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="9cf16-103">HASCATEGORY Function</span></span>

<span data-ttu-id="9cf16-104">Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.</span><span class="sxs-lookup"><span data-stu-id="9cf16-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="9cf16-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="9cf16-105">Version Information</span></span>

<span data-ttu-id="9cf16-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="9cf16-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9cf16-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cf16-107">Syntax</span></span>

<span data-ttu-id="9cf16-108">HASCATEGORY(\*\* *category* \*\* )</span><span class="sxs-lookup"><span data-stu-id="9cf16-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9cf16-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cf16-109">Parameters</span></span>

|<span data-ttu-id="9cf16-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9cf16-110">**Name**</span></span>|<span data-ttu-id="9cf16-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9cf16-111">**Required/Optional**</span></span>|<span data-ttu-id="9cf16-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9cf16-112">**Data Type**</span></span>|<span data-ttu-id="9cf16-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="9cf16-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9cf16-114">_category_</span><span class="sxs-lookup"><span data-stu-id="9cf16-114">_category_</span></span> <br/> |<span data-ttu-id="9cf16-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9cf16-115">Required</span></span>  <br/> |<span data-ttu-id="9cf16-116">**String**</span><span class="sxs-lookup"><span data-stu-id="9cf16-116">**String**</span></span> <br/> |<span data-ttu-id="9cf16-117">Catégorie à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9cf16-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9cf16-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9cf16-118">Return value</span></span>

 <span data-ttu-id="9cf16-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9cf16-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cf16-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cf16-120">Remarks</span></span>

 <span data-ttu-id="9cf16-121">*Les catégories*  sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes.</span><span class="sxs-lookup"><span data-stu-id="9cf16-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="9cf16-122">Vous pouvez définir les catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9cf16-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="9cf16-123">Vous pouvez définir plusieurs catégories pour une forme en les séparant par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="9cf16-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

