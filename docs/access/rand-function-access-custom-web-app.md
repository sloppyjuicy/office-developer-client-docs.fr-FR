---
title: RAND, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Renvoie un nombre pseudo-aléatoire compris entre 0 et 1.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781964"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="3f58e-103">RAND, fonction (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="3f58e-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="3f58e-104">Renvoie un nombre pseudo-aléatoire compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="3f58e-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3f58e-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="3f58e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3f58e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f58e-107">Syntax</span></span>

 <span data-ttu-id="3f58e-108">**RAND** ([ *Départ* ])</span><span class="sxs-lookup"><span data-stu-id="3f58e-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="3f58e-109">La fonction **Rand** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="3f58e-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="3f58e-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="3f58e-110">**Argument name**</span></span>|<span data-ttu-id="3f58e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f58e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3f58e-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="3f58e-112">*Seed*</span></span>  <br/> |<span data-ttu-id="3f58e-113">Entier qui donne la valeur de départ.</span><span class="sxs-lookup"><span data-stu-id="3f58e-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="3f58e-114">Si la *valeur de départ* n’est pas spécifié, une valeur de départ est affectée au hasard.</span><span class="sxs-lookup"><span data-stu-id="3f58e-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f58e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f58e-115">Remarks</span></span>

<span data-ttu-id="3f58e-116">Les appels de la fonction **Rand** avec la même valeur initiale répétitives retournent les mêmes résultats.</span><span class="sxs-lookup"><span data-stu-id="3f58e-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

