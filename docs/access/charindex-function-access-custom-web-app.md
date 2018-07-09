---
title: Fonction CharIndex (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Recherche une expression de texte pour une autre expression de texte et renvoie son démarrage position si trouvé.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781837"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="8adab-103">Fonction CharIndex (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="8adab-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="8adab-104">Recherche une expression de texte pour une autre expression de texte et renvoie son démarrage position si trouvé.</span><span class="sxs-lookup"><span data-stu-id="8adab-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8adab-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="8adab-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8adab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8adab-107">Syntax</span></span>

<span data-ttu-id="8adab-108">**CharIndex** (*TextExpression*, *WithinText*, [*Démarrer*])</span><span class="sxs-lookup"><span data-stu-id="8adab-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="8adab-109">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="8adab-109">**Argument Name**</span></span>|<span data-ttu-id="8adab-110">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8adab-110">**Required**</span></span>|<span data-ttu-id="8adab-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8adab-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8adab-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="8adab-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="8adab-113">Oui</span><span class="sxs-lookup"><span data-stu-id="8adab-113">Yes</span></span>  <br/> |<span data-ttu-id="8adab-114">Une expression de texte qui contient le texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="8adab-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="8adab-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="8adab-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="8adab-116">Oui</span><span class="sxs-lookup"><span data-stu-id="8adab-116">Yes</span></span>  <br/> |<span data-ttu-id="8adab-117">L’expression de texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="8adab-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="8adab-118">*Début*</span><span class="sxs-lookup"><span data-stu-id="8adab-118">*Start*</span></span>  <br/> |<span data-ttu-id="8adab-119">Non</span><span class="sxs-lookup"><span data-stu-id="8adab-119">No</span></span>  <br/> |<span data-ttu-id="8adab-120">Entier qui spécifie l’emplacement dans *WithinText* pour commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="8adab-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="8adab-121">Si *Démarrer* n’est pas spécifié, est un nombre négatif ou est égale à 0, la recherche commence au début de *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="8adab-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8adab-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="8adab-122">Remarks</span></span>

<span data-ttu-id="8adab-123">Si *TextExpression* ou *WithinText* est NULL, *CharIndex* renvoie la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="8adab-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="8adab-124">Si *TextExpression* est introuvable dans *WithinText*, *CharIndex* renvoie la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="8adab-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="8adab-125">La position de départ retournée est de base 1, et non de base 0.</span><span class="sxs-lookup"><span data-stu-id="8adab-125">The starting position returned is 1-based, not 0-based.</span></span>
  

