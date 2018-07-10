---
title: Action de SetReturnVar Macro (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: L’action SetReturnVar crée une variable de renvoi et lui affecte une valeur spécifique.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782004"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="68328-103">Action de SetReturnVar Macro (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="68328-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="68328-104">L’action **SetReturnVar** crée une variable de renvoi et lui affecte une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="68328-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="68328-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="68328-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="68328-107">L’action **SetReturnVar** est disponible uniquement dans les Macros de données.</span><span class="sxs-lookup"><span data-stu-id="68328-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="68328-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="68328-108">Setting</span></span>

<span data-ttu-id="68328-109">L’action **SetReturnVar** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="68328-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="68328-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="68328-110">**Argument name**</span></span>|<span data-ttu-id="68328-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="68328-111">**Required**</span></span>|<span data-ttu-id="68328-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="68328-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="68328-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="68328-113">_Name_</span></span> <br/> |<span data-ttu-id="68328-114">Oui</span><span class="sxs-lookup"><span data-stu-id="68328-114">Yes</span></span>  <br/> |<span data-ttu-id="68328-115">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="68328-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="68328-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="68328-116">_Expression_</span></span> <br/> |<span data-ttu-id="68328-117">Oui</span><span class="sxs-lookup"><span data-stu-id="68328-117">Yes</span></span>  <br/> |<span data-ttu-id="68328-118">Une expression qui sera utilisée pour définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="68328-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="68328-119">Ne faites pas précéder l’expression avec le signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="68328-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="68328-120">Vous pouvez cliquer sur le bouton **Générer** pour utiliser le **Générateur d’Expression** pour définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="68328-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68328-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="68328-121">Remarks</span></span>

<span data-ttu-id="68328-122">L’action **SetReturnVar** est utilisée pour créer un **ReturnVar**, qui est la variable peut être utilisé par des macros qui appeler une macro de données à l’aide de l’action **ExécuterMacroDonnées** .</span><span class="sxs-lookup"><span data-stu-id="68328-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="68328-123">Une fois un **ReturnVar** est créé par l’action **SetReturnVar** , la macro appelante peut l’utiliser dans une expression.</span><span class="sxs-lookup"><span data-stu-id="68328-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="68328-124">Par exemple, si vous avez créé un **ReturnVar** nommé **UpdateSuccess**, vous pouvez utiliser la variable à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="68328-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="68328-125">L’action **SetReturnVar** peut être utilisée uniquement dans les macros de données nommée.</span><span class="sxs-lookup"><span data-stu-id="68328-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="68328-126">Il n’est pas disponible dans les macros de données associées à un événement de macro de données.</span><span class="sxs-lookup"><span data-stu-id="68328-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

