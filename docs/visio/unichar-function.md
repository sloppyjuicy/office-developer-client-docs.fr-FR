---
title: UNICHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Renvoie le caractère Unicode d'un nombre.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327346"
---
# <a name="unichar-function"></a><span data-ttu-id="5d93a-103">Fonction UNICHAR</span><span class="sxs-lookup"><span data-stu-id="5d93a-103">UNICHAR Function</span></span>

<span data-ttu-id="5d93a-104">Renvoie le caractère Unicode d'un nombre.</span><span class="sxs-lookup"><span data-stu-id="5d93a-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5d93a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d93a-105">Syntax</span></span>

<span data-ttu-id="5d93a-106">UNICHAR (\* \* *nombre* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5d93a-106">UNICHAR (\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d93a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d93a-107">Parameters</span></span>

|<span data-ttu-id="5d93a-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5d93a-108">**Name**</span></span>|<span data-ttu-id="5d93a-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="5d93a-109">**Required/Optional**</span></span>|<span data-ttu-id="5d93a-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="5d93a-110">**Data Type**</span></span>|<span data-ttu-id="5d93a-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="5d93a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d93a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="5d93a-112">_number_</span></span> <br/> |<span data-ttu-id="5d93a-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5d93a-113">Required</span></span>  <br/> |<span data-ttu-id="5d93a-114">**Entier**</span><span class="sxs-lookup"><span data-stu-id="5d93a-114">**Integer**</span></span> <br/> |<span data-ttu-id="5d93a-115">Entier compris entre 1 et 65 535 (inclus), ou la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="5d93a-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d93a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d93a-116">Remarks</span></span>

<span data-ttu-id="5d93a-117">La chaîne obtenue présente une longueur d’un caractère unicode (deux caractères).</span><span class="sxs-lookup"><span data-stu-id="5d93a-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5d93a-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="5d93a-118">Example</span></span>

<span data-ttu-id="5d93a-119">UNICHAR (65)</span><span class="sxs-lookup"><span data-stu-id="5d93a-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="5d93a-120">Renvoie A (lettre majuscule latine A)</span><span class="sxs-lookup"><span data-stu-id="5d93a-120">Returns A (Latin Capital Letter A)</span></span> 
  

