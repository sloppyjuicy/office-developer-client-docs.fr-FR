---
title: GETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424328"
---
# <a name="getref-function"></a><span data-ttu-id="19a40-103">Fonction GETREF</span><span class="sxs-lookup"><span data-stu-id="19a40-103">GETREF Function</span></span>

<span data-ttu-id="19a40-104">Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.</span><span class="sxs-lookup"><span data-stu-id="19a40-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="19a40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19a40-105">Syntax</span></span>

<span data-ttu-id="19a40-106">GETREF(\*\* *cellname* \*\* )</span><span class="sxs-lookup"><span data-stu-id="19a40-106">GETREF(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="19a40-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19a40-107">Parameters</span></span>

|<span data-ttu-id="19a40-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="19a40-108">**Name**</span></span>|<span data-ttu-id="19a40-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="19a40-109">**Required/Optional**</span></span>|<span data-ttu-id="19a40-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="19a40-110">**Data Type**</span></span>|<span data-ttu-id="19a40-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="19a40-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="19a40-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="19a40-112">_cellname_</span></span> <br/> |<span data-ttu-id="19a40-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="19a40-113">Required</span></span>  <br/> |<span data-ttu-id="19a40-114">**String**</span><span class="sxs-lookup"><span data-stu-id="19a40-114">**String**</span></span> <br/> |<span data-ttu-id="19a40-115">Nom de la cellule à qui obtenir une référence.</span><span class="sxs-lookup"><span data-stu-id="19a40-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="19a40-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="19a40-116">Example</span></span>

<span data-ttu-id="19a40-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="19a40-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="19a40-118">Donne à la formule de la cellule PinX la valeur 5,1.</span><span class="sxs-lookup"><span data-stu-id="19a40-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

