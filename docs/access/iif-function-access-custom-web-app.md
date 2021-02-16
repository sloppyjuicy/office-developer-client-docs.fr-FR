---
title: Fonction IIf (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Vérifie si une condition est remplie et renvoie une valeur si TRUE d’une autre sur si elle est FALSE.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439078"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="dff35-103">Fonction IIf (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="dff35-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="dff35-104">Vérifie si une condition est remplie et renvoie une valeur si TRUE d’une autre sur si elle est FALSE.</span><span class="sxs-lookup"><span data-stu-id="dff35-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dff35-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="dff35-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dff35-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dff35-107">Syntax</span></span>

<span data-ttu-id="dff35-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="dff35-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="dff35-109">La **fonction IIf** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="dff35-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="dff35-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="dff35-110">**Argument name**</span></span>|<span data-ttu-id="dff35-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="dff35-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dff35-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="dff35-112">*Condition*</span></span>  <br/> |<span data-ttu-id="dff35-113">Expression que vous souhaitez évaluer.</span><span class="sxs-lookup"><span data-stu-id="dff35-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="dff35-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="dff35-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="dff35-115">Valeur ou expression renvoyée si  *la condition*  a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="dff35-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="dff35-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="dff35-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="dff35-117">Valeur ou expression renvoyée si  *la condition*  est False.</span><span class="sxs-lookup"><span data-stu-id="dff35-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="dff35-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="dff35-118">Example</span></span>

<span data-ttu-id="dff35-119">L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName.</span><span class="sxs-lookup"><span data-stu-id="dff35-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="dff35-120">Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.</span><span class="sxs-lookup"><span data-stu-id="dff35-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


