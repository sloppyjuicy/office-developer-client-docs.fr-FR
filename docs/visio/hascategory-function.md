---
title: HASCATEGORY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788765"
---
# <a name="hascategory-function"></a><span data-ttu-id="ed8b1-103">HASCATEGORY, fonction</span><span class="sxs-lookup"><span data-stu-id="ed8b1-103">HASCATEGORY Function</span></span>

<span data-ttu-id="ed8b1-104">Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.</span><span class="sxs-lookup"><span data-stu-id="ed8b1-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="ed8b1-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="ed8b1-105">Version Information</span></span>

<span data-ttu-id="ed8b1-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="ed8b1-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed8b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed8b1-107">Syntax</span></span>

<span data-ttu-id="ed8b1-108">HASCATEGORY (** *catégorie* **)</span><span class="sxs-lookup"><span data-stu-id="ed8b1-108">HASCATEGORY(** *category* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed8b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed8b1-109">Parameters</span></span>

|<span data-ttu-id="ed8b1-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ed8b1-110">**Name**</span></span>|<span data-ttu-id="ed8b1-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ed8b1-111">**Required/Optional**</span></span>|<span data-ttu-id="ed8b1-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ed8b1-112">**Data Type**</span></span>|<span data-ttu-id="ed8b1-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="ed8b1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed8b1-114">_category_</span><span class="sxs-lookup"><span data-stu-id="ed8b1-114">_category_</span></span> <br/> |<span data-ttu-id="ed8b1-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ed8b1-115">Required</span></span>  <br/> |<span data-ttu-id="ed8b1-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed8b1-116">**String**</span></span> <br/> |<span data-ttu-id="ed8b1-117">Catégorie à rechercher.</span><span class="sxs-lookup"><span data-stu-id="ed8b1-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ed8b1-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ed8b1-118">Return value</span></span>

 <span data-ttu-id="ed8b1-119">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="ed8b1-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed8b1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ed8b1-120">Remarks</span></span>

 <span data-ttu-id="ed8b1-121">*Les catégories* sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes.</span><span class="sxs-lookup"><span data-stu-id="ed8b1-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="ed8b1-122">Vous pouvez définir des catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme.</span><span class="sxs-lookup"><span data-stu-id="ed8b1-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="ed8b1-123">Vous pouvez définir plusieurs catégories d’une forme en séparant les catégories par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="ed8b1-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

