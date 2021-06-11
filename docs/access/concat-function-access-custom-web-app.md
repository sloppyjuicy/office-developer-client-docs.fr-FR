---
title: Fonction Concat (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423271"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="ecc1a-103">Fonction Concat (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="ecc1a-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="ecc1a-104">Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ecc1a-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ecc1a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecc1a-107">Syntax</span></span>

<span data-ttu-id="ecc1a-108">**Concat** (*Valeur1*, *Valeur2*, ... [*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="ecc1a-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="ecc1a-109">La **fonction Concat** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ecc1a-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="ecc1a-110">**Argument Name**</span></span>|<span data-ttu-id="ecc1a-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ecc1a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ecc1a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecc1a-112">Value</span></span>  <br/> |<span data-ttu-id="ecc1a-113">Valeur de chaîne à concaténer aux autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecc1a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ecc1a-114">Remarks</span></span>

<span data-ttu-id="ecc1a-115">**Concat** prend un nombre variable d’arguments de chaîne et les concatène en une seule chaîne.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-115">**Concat** takes a variable number of string arguments and concatenates them into a single string.</span></span> <span data-ttu-id="ecc1a-116">Un minimum de deux arguments de chaîne est requis ; Dans le cas contraire, une erreur est produite.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-116">A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="ecc1a-117">Tous les arguments sont implicitement convertis en types de données de chaîne, puis concatés.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="ecc1a-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="ecc1a-118">Example</span></span>

<span data-ttu-id="ecc1a-119">L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="ecc1a-120">Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.</span><span class="sxs-lookup"><span data-stu-id="ecc1a-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


