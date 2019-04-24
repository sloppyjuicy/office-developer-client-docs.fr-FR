---
title: Fonction IIf (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Vérifie si une condition est remplie et renvoie une valeur si la valeur est TRUE si elle a la valeur FALSe.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301861"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="bfd27-103">Fonction IIf (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="bfd27-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="bfd27-104">Vérifie si une condition est remplie et renvoie une valeur si la valeur est TRUE si elle a la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="bfd27-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bfd27-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="bfd27-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bfd27-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfd27-107">Syntax</span></span>

<span data-ttu-id="bfd27-108">**VraiFaux (IIF** ) (*Condition*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="bfd27-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="bfd27-109">La fonction **IIf** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="bfd27-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="bfd27-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="bfd27-110">**Argument name**</span></span>|<span data-ttu-id="bfd27-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="bfd27-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bfd27-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="bfd27-112">*Condition*</span></span>  <br/> |<span data-ttu-id="bfd27-113">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="bfd27-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="bfd27-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="bfd27-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="bfd27-115">Valeur ou expression renvoyée si la *condition* est vraie.</span><span class="sxs-lookup"><span data-stu-id="bfd27-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="bfd27-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="bfd27-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="bfd27-117">Valeur ou expression renvoyée si la *condition* a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="bfd27-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="bfd27-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="bfd27-118">Example</span></span>

<span data-ttu-id="bfd27-119">L'expression suivante peut être utilisée pour afficher le nom complet d'une personne dans laquelle le tableau contient les champs FirstName, MiddleInitial et LastName.</span><span class="sxs-lookup"><span data-stu-id="bfd27-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="bfd27-120">Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.</span><span class="sxs-lookup"><span data-stu-id="bfd27-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


