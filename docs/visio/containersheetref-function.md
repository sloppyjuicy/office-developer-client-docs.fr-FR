---
title: CONTAINERSHEETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Renvoie une référence de feuille au conteneur spécifié contenant la forme.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318983"
---
# <a name="containersheetref-function"></a><span data-ttu-id="3f8a7-103">Fonction CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="3f8a7-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="3f8a7-104">Renvoie une référence de feuille au conteneur spécifié contenant la forme.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="3f8a7-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="3f8a7-105">Version Information</span></span>

<span data-ttu-id="3f8a7-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="3f8a7-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3f8a7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f8a7-107">Syntax</span></span>

<span data-ttu-id="3f8a7-108">CONTAINERSHEETREF (\* \* *index* \* \* \* \* *[, Category]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3f8a7-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3f8a7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f8a7-109">Parameters</span></span>

|<span data-ttu-id="3f8a7-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3f8a7-110">**Name**</span></span>|<span data-ttu-id="3f8a7-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3f8a7-111">**Required/Optional**</span></span>|<span data-ttu-id="3f8a7-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3f8a7-112">**Data Type**</span></span>|<span data-ttu-id="3f8a7-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f8a7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3f8a7-114">_index_</span><span class="sxs-lookup"><span data-stu-id="3f8a7-114">_index_</span></span> <br/> |<span data-ttu-id="3f8a7-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3f8a7-115">Required</span></span>  <br/> |<span data-ttu-id="3f8a7-116">**Entier**</span><span class="sxs-lookup"><span data-stu-id="3f8a7-116">**Integer**</span></span> <br/> |<span data-ttu-id="3f8a7-117">Index de base 1 du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-117">The 1-based index of the container.</span></span> <span data-ttu-id="3f8a7-118">Voir la section Remarques pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="3f8a7-119">_catégories_</span><span class="sxs-lookup"><span data-stu-id="3f8a7-119">_category_</span></span> <br/> |<span data-ttu-id="3f8a7-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3f8a7-120">Optional</span></span>  <br/> |<span data-ttu-id="3f8a7-121">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f8a7-121">**String**</span></span> <br/> |<span data-ttu-id="3f8a7-122">Catégorie du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-122">The category of the container.</span></span> <span data-ttu-id="3f8a7-123">Voir la section Remarques pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3f8a7-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f8a7-124">Return value</span></span>

<span data-ttu-id="3f8a7-125">Référence ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="3f8a7-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f8a7-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f8a7-126">Remarks</span></span>

<span data-ttu-id="3f8a7-127">L’index d’un conteneur est calculé en fonction de l’ordre de plan des conteneurs d’avant en arrière.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="3f8a7-128">Les *catégories* sont des chaînes définies par l'utilisateur que vous pouvez utiliser pour catégoriser les formes.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="3f8a7-129">Vous pouvez définir les catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="3f8a7-130">Vous pouvez définir plusieurs catégories pour une forme en les séparant par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="3f8a7-131">Si la forme n’est pas membre d’un conteneur, ou si aucun conteneur ne correspond à l’index spécifié et à la catégorie, CONTAINERSHEETREF renvoie #REF!.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="3f8a7-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f8a7-132">Example</span></span>

<span data-ttu-id="3f8a7-133">CONTAINERSHEETREF (1)! Standard</span><span class="sxs-lookup"><span data-stu-id="3f8a7-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="3f8a7-134">Renvoie la valeur de la cellule Height du conteneur le plus en avant sur la page à laquelle appartient la forme.</span><span class="sxs-lookup"><span data-stu-id="3f8a7-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

