---
title: SetField Macro Action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: L'action DéfinirChamp peut être utilisée pour assigner une valeur à un champ.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432925"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="a7b12-103">SetField Macro Action (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="a7b12-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="a7b12-104">L'action **DéfinirChamp** peut être utilisée pour assigner une valeur à un champ.</span><span class="sxs-lookup"><span data-stu-id="a7b12-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a7b12-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="a7b12-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a7b12-107">L’action **DéfinirChamp** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="a7b12-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="a7b12-108">Setting</span><span class="sxs-lookup"><span data-stu-id="a7b12-108">Setting</span></span>

<span data-ttu-id="a7b12-109">L’action **DéfinirChamp** utilise les arguments répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7b12-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="a7b12-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="a7b12-110">**Argument name**</span></span>|<span data-ttu-id="a7b12-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7b12-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7b12-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a7b12-112">**Name**</span></span> <br/> |<span data-ttu-id="a7b12-113">Chaîne qui identifie le champ.</span><span class="sxs-lookup"><span data-stu-id="a7b12-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="a7b12-114">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a7b12-114">**Value**</span></span> <br/> |<span data-ttu-id="a7b12-115">Expression qui spécifie la valeur à affecter au champ.</span><span class="sxs-lookup"><span data-stu-id="a7b12-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7b12-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7b12-116">Remarks</span></span>

<span data-ttu-id="a7b12-117">**L’action DéfinirField** ne peut pas être utilisée en dehors d’un bloc de données **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** ou **[EditRecord.](editrecord-data-block-access-custom-web-app.md)**</span><span class="sxs-lookup"><span data-stu-id="a7b12-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

