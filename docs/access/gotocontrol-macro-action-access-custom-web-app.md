---
title: Action de macro AtteindreContrôle (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Vous pouvez utiliser l’action AtteindreContrôle pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302575"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="4b1c2-103">Action de macro AtteindreContrôle (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="4b1c2-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="4b1c2-104">Vous pouvez utiliser l’action **AtteindreContrôle** pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4b1c2-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4b1c2-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="4b1c2-107">Setting</span></span>

<span data-ttu-id="4b1c2-108">L’action **AtteindreContrôle** possède l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="4b1c2-109">**Argument de l’action**</span><span class="sxs-lookup"><span data-stu-id="4b1c2-109">**Action argument**</span></span>|<span data-ttu-id="4b1c2-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b1c2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b1c2-111">**Nom du contrôle** :</span><span class="sxs-lookup"><span data-stu-id="4b1c2-111">**Control Name**</span></span> <br/> |<span data-ttu-id="4b1c2-112">Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="4b1c2-113">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b1c2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b1c2-114">Remarks</span></span>

<span data-ttu-id="4b1c2-115">Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="4b1c2-116">Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="4b1c2-117">Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.</span><span class="sxs-lookup"><span data-stu-id="4b1c2-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

