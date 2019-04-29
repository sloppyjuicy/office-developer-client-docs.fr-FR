---
title: SetReturnVar, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: L'action SetReturnVar crée une variable de retour et lui affecte une valeur spécifique.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409593"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="9b8af-103">SetReturnVar, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="9b8af-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="9b8af-104">L'action **SetReturnVar** crée une variable de retour et lui affecte une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="9b8af-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9b8af-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="9b8af-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b8af-107">L'action **SetReturnVar** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="9b8af-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="9b8af-108">Setting</span><span class="sxs-lookup"><span data-stu-id="9b8af-108">Setting</span></span>

<span data-ttu-id="9b8af-109">L'action **SetReturnVar** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="9b8af-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="9b8af-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="9b8af-110">**Argument name**</span></span>|<span data-ttu-id="9b8af-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9b8af-111">**Required**</span></span>|<span data-ttu-id="9b8af-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b8af-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9b8af-113">_Nom_</span><span class="sxs-lookup"><span data-stu-id="9b8af-113">_Name_</span></span> <br/> |<span data-ttu-id="9b8af-114">Oui</span><span class="sxs-lookup"><span data-stu-id="9b8af-114">Yes</span></span>  <br/> |<span data-ttu-id="9b8af-115">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="9b8af-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="9b8af-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="9b8af-116">_Expression_</span></span> <br/> |<span data-ttu-id="9b8af-117">Oui</span><span class="sxs-lookup"><span data-stu-id="9b8af-117">Yes</span></span>  <br/> |<span data-ttu-id="9b8af-118">Expression destiné à être utilisé pour définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="9b8af-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="9b8af-119">Ne faites pas précéder l’expression d’un signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="9b8af-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="9b8af-120">Vous pouvez cliquer sur le bouton **Générer** afin d’utiliser le **Générateur d’expressions** pour définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="9b8af-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b8af-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="9b8af-121">Remarks</span></span>

<span data-ttu-id="9b8af-122">L'action **SetReturnVar** est utilisée pour créer une **ReturnVar**, variable qui peut être utilisée par les macros qui appellent une macro de données à l'aide de l'action **RunDataMacro** .</span><span class="sxs-lookup"><span data-stu-id="9b8af-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="9b8af-123">Une fois qu'une **ReturnVar** a été créée par l'action **SetReturnVar** , la macro appelante peut l'utiliser dans une expression.</span><span class="sxs-lookup"><span data-stu-id="9b8af-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="9b8af-124">Par exemple, si vous avez créé un **ReturnVar** nommé **UpdateSuccess**, vous pouvez utiliser la variable à l'aide de la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="9b8af-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="9b8af-125">L'action **SetReturnVar** peut être utilisée uniquement dans les macros de données nommées.</span><span class="sxs-lookup"><span data-stu-id="9b8af-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="9b8af-126">Elle n'est pas disponible dans les macros de données qui sont attachées à un événement de macro de données.</span><span class="sxs-lookup"><span data-stu-id="9b8af-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

