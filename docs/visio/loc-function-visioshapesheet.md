---
title: LOC Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Prend un point défini dans les coordonnées locales d'une forme et renvoie le point équivalent exprimé dans les coordonnées locales de la forme associée à la formule.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422424"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="d7fb1-103">LOC Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d7fb1-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d7fb1-104">Prend un point défini dans les coordonnées locales d'une forme et renvoie le point équivalent exprimé dans les coordonnées locales de la forme associée à la formule.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d7fb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7fb1-105">Syntax</span></span>

<span data-ttu-id="d7fb1-106">LOC (\* \* *point* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d7fb1-106">LOC(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d7fb1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7fb1-107">Parameters</span></span>

|<span data-ttu-id="d7fb1-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d7fb1-108">**Name**</span></span>|<span data-ttu-id="d7fb1-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d7fb1-109">**Required/Optional**</span></span>|<span data-ttu-id="d7fb1-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d7fb1-110">**Data Type**</span></span>|<span data-ttu-id="d7fb1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7fb1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d7fb1-112">_virgule_</span><span class="sxs-lookup"><span data-stu-id="d7fb1-112">_point_</span></span> <br/> |<span data-ttu-id="d7fb1-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7fb1-113">Required</span></span>  <br/> |<span data-ttu-id="d7fb1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d7fb1-114">**String**</span></span> <br/> | <span data-ttu-id="d7fb1-115">Point défini dans les coordonnées locales d’une forme.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d7fb1-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7fb1-116">Return value</span></span>

<span data-ttu-id="d7fb1-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d7fb1-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7fb1-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7fb1-118">Remarks</span></span>

<span data-ttu-id="d7fb1-p101">Les coordonnées locales sont mesurées à partir du coin inférieur gauche du rectangle de sélection de la forme. Les deux formes doivent figurer sur la même page.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-p101">Local coordinates are measured from the lower-left corner of the shape's selection rectangle. Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="d7fb1-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="d7fb1-121">Example</span></span>

<span data-ttu-id="d7fb1-122">LOC (PNT (Sheet. 5! LocPinX, Sheet. 5! LocPinY))</span><span class="sxs-lookup"><span data-stu-id="d7fb1-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="d7fb1-p102">Dans cette expression, PNT convertit un ensemble de coordonnées locales de Feuille.5 en un point (Feuille.5 est une autre forme sur la même page de dessin). LOC convertit ensuite ce point en un point équivalent dans le système de coordonnées locales de la forme active en se basant sur le coin inférieur gauche du rectangle de sélection de la forme active.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-p102">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point. (Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="d7fb1-125">Le chiffre 5 de la Feuille.5 est l’identificateur de la forme, tel qu’il s’affiche dans la boîte de dialogue **Nom de la forme** (onglet **Développeur**).</span><span class="sxs-lookup"><span data-stu-id="d7fb1-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

