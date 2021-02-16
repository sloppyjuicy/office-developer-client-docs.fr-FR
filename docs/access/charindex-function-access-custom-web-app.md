---
title: Fonction CharIndex (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Recherche une autre expression de texte dans une expression de texte et renvoie sa position de départ si elle est trouvée.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423131"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="d0c6e-103">Fonction CharIndex (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="d0c6e-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="d0c6e-104">Recherche une autre expression de texte dans une expression de texte et renvoie sa position de départ si elle est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d0c6e-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d0c6e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0c6e-107">Syntax</span></span>

<span data-ttu-id="d0c6e-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="d0c6e-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="d0c6e-109">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="d0c6e-109">**Argument Name**</span></span>|<span data-ttu-id="d0c6e-110">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d0c6e-110">**Required**</span></span>|<span data-ttu-id="d0c6e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0c6e-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d0c6e-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="d0c6e-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="d0c6e-113">Oui</span><span class="sxs-lookup"><span data-stu-id="d0c6e-113">Yes</span></span>  <br/> |<span data-ttu-id="d0c6e-114">Expression de texte qui contient le texte à trouver.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="d0c6e-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="d0c6e-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="d0c6e-116">Oui</span><span class="sxs-lookup"><span data-stu-id="d0c6e-116">Yes</span></span>  <br/> |<span data-ttu-id="d0c6e-117">Expression de texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="d0c6e-118">*Démarrage*</span><span class="sxs-lookup"><span data-stu-id="d0c6e-118">*Start*</span></span>  <br/> |<span data-ttu-id="d0c6e-119">Non</span><span class="sxs-lookup"><span data-stu-id="d0c6e-119">No</span></span>  <br/> |<span data-ttu-id="d0c6e-120">Nombre intégral qui spécifie l’emplacement dans  *WithinText*  pour commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="d0c6e-121">Si  *l’indication*  Start n’est pas spécifiée, est un nombre négatif ou est 0, la recherche commence au début de  *WithinText*  .</span><span class="sxs-lookup"><span data-stu-id="d0c6e-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0c6e-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0c6e-122">Remarks</span></span>

<span data-ttu-id="d0c6e-123">Si  *TextExpression ou*  *WithinText*  a la valeur NULL,  *CharIndex renvoie*  la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="d0c6e-124">Si  *TextExpression n’est*  pas trouvé  *dans WithinText*,  *CharIndex renvoie*  0.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="d0c6e-125">La position de départ renvoyée est basée sur 1, et non sur 0.</span><span class="sxs-lookup"><span data-stu-id="d0c6e-125">The starting position returned is 1-based, not 0-based.</span></span>
  

