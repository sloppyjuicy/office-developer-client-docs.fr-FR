---
title: Action de Macro DéfinirPropriété (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Vous pouvez utiliser l’action DéfinirPropriété pour définir une propriété d’un contrôle sur un affichage.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781975"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="4fc2f-103">Action de Macro DéfinirPropriété (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="4fc2f-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="4fc2f-104">Vous pouvez utiliser l’action **DéfinirPropriété** pour définir une propriété d’un contrôle sur un affichage.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4fc2f-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4fc2f-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fc2f-107">Setting</span></span>

<span data-ttu-id="4fc2f-108">L’action **DéfinirPropriété** utilise les arguments répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="4fc2f-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="4fc2f-109">**Action argument**</span></span>|<span data-ttu-id="4fc2f-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="4fc2f-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4fc2f-111">_Nom du contrôle_</span><span class="sxs-lookup"><span data-stu-id="4fc2f-111">_Control Name_</span></span> <br/> |<span data-ttu-id="4fc2f-112">Tapez le nom du champ ou du contrôle pour lequel vous voulez définir la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="4fc2f-113">Laissez cet argument vide pour définir la propriété pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="4fc2f-114">_Propriété_</span><span class="sxs-lookup"><span data-stu-id="4fc2f-114">_Property_</span></span> <br/> |<span data-ttu-id="4fc2f-115">Sélectionnez la propriété que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-115">Select the property that you want to set.</span></span> <span data-ttu-id="4fc2f-116">Voir la section **Remarques** dans cet article pour obtenir la liste des propriétés qui peuvent être définies à l’aide de cette action.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-116">See the **Remarks** section in this article for a list of the properties that can be set by using this action.</span></span>  <br/> |
| <span data-ttu-id="4fc2f-117">_Valeur_</span><span class="sxs-lookup"><span data-stu-id="4fc2f-117">_Value_</span></span> <br/> |<span data-ttu-id="4fc2f-118">Tapez la valeur de la propriété doit être définie sur.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-118">Type the value that the property is to be set to.</span></span> <span data-ttu-id="4fc2f-119">Pour les propriétés dont les valeurs sont Oui ou non, utilisent **-1** pour Oui et **0** pour non.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-119">For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fc2f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4fc2f-120">Remarks</span></span>

<span data-ttu-id="4fc2f-121">Vous pouvez utiliser l’action **DéfinirPropriété** pour définir les propriétés d’un contrôle suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fc2f-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="4fc2f-122">Caption</span><span class="sxs-lookup"><span data-stu-id="4fc2f-122">Caption</span></span>
    
- <span data-ttu-id="4fc2f-123">Activé</span><span class="sxs-lookup"><span data-stu-id="4fc2f-123">Enabled</span></span>
    
- <span data-ttu-id="4fc2f-124">Propriété ForeColor</span><span class="sxs-lookup"><span data-stu-id="4fc2f-124">ForeColor</span></span>
    
- <span data-ttu-id="4fc2f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fc2f-125">Value</span></span>
    
- <span data-ttu-id="4fc2f-126">Visible</span><span class="sxs-lookup"><span data-stu-id="4fc2f-126">Visible</span></span>
    
<span data-ttu-id="4fc2f-127">Si vous entrez une valeur non admise pour l'argument ** *Valeur* **, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l'interprétation de l'argument.</span><span class="sxs-lookup"><span data-stu-id="4fc2f-127">If you enter an invalid value for the ** *Value* ** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

