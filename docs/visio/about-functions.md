---
title: À propos des fonctions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
localization_priority: Normal
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: "Une fonction effectue une tâche unique et bien précise. La plupart des fonctions acceptent plusieurs arguments comme entrées. Le type et le nombre d'arguments dépendent des fonctions, mais toutes utilisent la même syntaxe générale :"
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415977"
---
# <a name="about-functions"></a><span data-ttu-id="bcee1-105">À propos des fonctions</span><span class="sxs-lookup"><span data-stu-id="bcee1-105">About Functions</span></span>

<span data-ttu-id="bcee1-p102">Une fonction effectue une tâche unique et bien précise. La plupart des fonctions acceptent plusieurs arguments comme entrées. Le type et le nombre d'arguments dépendent des fonctions, mais toutes utilisent la même syntaxe générale :</span><span class="sxs-lookup"><span data-stu-id="bcee1-p102">A function performs a single well-defined task. Most functions take a number of arguments as input. Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="bcee1-109">**FUNCTION(** _argument1_,  _argument2_, ...</span><span class="sxs-lookup"><span data-stu-id="bcee1-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="bcee1-110">_argumentN_ [, _argumentA_  |   _argument_ **])**</span><span class="sxs-lookup"><span data-stu-id="bcee1-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="bcee1-111">**Élément syntaxique**</span><span class="sxs-lookup"><span data-stu-id="bcee1-111">**Syntax element**</span></span>|<span data-ttu-id="bcee1-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="bcee1-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bcee1-113">( )</span><span class="sxs-lookup"><span data-stu-id="bcee1-113">( )</span></span>  <br/> | <span data-ttu-id="bcee1-114">Si une fonction n'accepte pas d'arguments, elle doit être suivie d'une paire de parenthèses vide ().</span><span class="sxs-lookup"><span data-stu-id="bcee1-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="bcee1-115">,</span><span class="sxs-lookup"><span data-stu-id="bcee1-115">,</span></span>  <br/> | <span data-ttu-id="bcee1-116">Les arguments sont séparés par une virgule.</span><span class="sxs-lookup"><span data-stu-id="bcee1-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="bcee1-117">...</span><span class="sxs-lookup"><span data-stu-id="bcee1-117">...</span></span>  <br/> | <span data-ttu-id="bcee1-118">Utilisé pour la notation uniquement ; ne pas inclure dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="bcee1-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="bcee1-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="bcee1-119">[ ]</span></span>  <br/> | <span data-ttu-id="bcee1-p104">Argument facultatif. Utilisé pour la notation uniquement ; ne pas inclure dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="bcee1-p104">Optional argument. Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="bcee1-122">Un choix ; vous pouvez inclure  _argumentA_ ou  _argument_.</span><span class="sxs-lookup"><span data-stu-id="bcee1-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="bcee1-123">Utilisé pour la notation uniquement ; ne pas inclure dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="bcee1-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="bcee1-p106">De nombreuses fonctions utilisables dans les formules ressemblent à celles que vous avez l'habitude de rencontrer dans les tableurs : fonctions mathématiques, comme SUM ou SQRT ; trigonométriques, comme SIN ou COS, ou logiques, comme IF ou NOT. Beaucoup d'autres fonctions sont toutefois propres à Microsoft Office Visio, par exemple GUARD, GRAVITY et RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="bcee1-p106">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT. Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="bcee1-126">Pour plus d'informations sur des fonctions spécifiques, reportez-vous à l'aide Référence ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="bcee1-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="bcee1-127">Certaines fonctions apparaissent dans les formules générées par  Visio, mais ne sont pas affichées dans la boîte de dialogue Modifier la formule ou décrites dans cette référence, car elles sont réservées à un usage interne et ne doivent pas être utilisées dans d’autres formules.</span><span class="sxs-lookup"><span data-stu-id="bcee1-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="bcee1-128">Voici quelques exemples : ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 et _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="bcee1-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

