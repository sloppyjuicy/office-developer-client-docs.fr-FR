---
title: SetProperty, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Vous pouvez utiliser l'action DéfinirPropriété pour définir une propriété pour un contrôle sur une vue.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307888"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="6fb17-103">SetProperty, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="6fb17-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="6fb17-104">Vous pouvez utiliser l'action **DéfinirPropriété** pour définir une propriété pour un contrôle sur une vue.</span><span class="sxs-lookup"><span data-stu-id="6fb17-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6fb17-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="6fb17-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="6fb17-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6fb17-107">Setting</span></span>

<span data-ttu-id="6fb17-108">L'action **SetProperty** possède les arguments figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6fb17-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="6fb17-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="6fb17-109">**Action argument**</span></span>|<span data-ttu-id="6fb17-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="6fb17-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6fb17-111">_Nom du contrôle_ :</span><span class="sxs-lookup"><span data-stu-id="6fb17-111">_Control Name_</span></span> <br/> |<span data-ttu-id="6fb17-112">Tapez le nom du champ ou du contrôle pour lequel vous souhaitez définir la valeur d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="6fb17-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="6fb17-113">Laissez cet argument vide pour définir la propriété de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="6fb17-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="6fb17-114">_Property_</span><span class="sxs-lookup"><span data-stu-id="6fb17-114">_Property_</span></span> <br/> |<span data-ttu-id="6fb17-p103">Sélectionnez la propriété dont la valeur doit être définie. Consultez la section **Remarques** de cet article pour accéder à la liste des propriétés qui peuvent être définies via cette action.</span><span class="sxs-lookup"><span data-stu-id="6fb17-p103">Select the property that you want to set. See the **Remarks** section in this article for a list of the properties that can be set by using this action.  </span></span><br/> |
| <span data-ttu-id="6fb17-117">_Valeur_</span><span class="sxs-lookup"><span data-stu-id="6fb17-117">_Value_</span></span> <br/> |<span data-ttu-id="6fb17-p104">Tapez la valeur que vous souhaitez définir pour la propriété. Pour les propriétés dont la valeur doit être définie sur Oui ou Non, utilisez **-1** pour Oui et **0** pour Non.</span><span class="sxs-lookup"><span data-stu-id="6fb17-p104">Type the value that the property is to be set to. For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fb17-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fb17-120">Remarks</span></span>

<span data-ttu-id="6fb17-121">Vous pouvez utiliser l'action **SetProperty** pour définir les propriétés suivantes d'un contrôle:</span><span class="sxs-lookup"><span data-stu-id="6fb17-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="6fb17-122">Légende</span><span class="sxs-lookup"><span data-stu-id="6fb17-122">Caption</span></span>
    
- <span data-ttu-id="6fb17-123">Activé</span><span class="sxs-lookup"><span data-stu-id="6fb17-123">Enabled</span></span>
    
- <span data-ttu-id="6fb17-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="6fb17-124">ForeColor</span></span>
    
- <span data-ttu-id="6fb17-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb17-125">Value</span></span>
    
- <span data-ttu-id="6fb17-126">Visible</span><span class="sxs-lookup"><span data-stu-id="6fb17-126">Visible</span></span>
    
<span data-ttu-id="6fb17-127">Si vous entrez une valeur non admise pour l'argument \*\* *Valeur* \*\*, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l'interprétation de l'argument.</span><span class="sxs-lookup"><span data-stu-id="6fb17-127">If you enter an invalid value for the \*\* *Value* \*\* argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

