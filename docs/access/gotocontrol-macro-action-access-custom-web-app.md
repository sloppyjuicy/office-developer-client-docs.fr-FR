---
title: Action de macro AtteindreContrôle (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Vous pouvez utiliser l’action AtteindreContrôle pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781814"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="0992d-103">Action de macro AtteindreContrôle (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="0992d-103">GoToControl Macro Action (Access 2013 custom web app)</span></span>

<span data-ttu-id="0992d-104">Vous pouvez utiliser l’action **AtteindreContrôle** pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.</span><span class="sxs-lookup"><span data-stu-id="0992d-104">You can use the GoToControl method to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0992d-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-FR/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="0992d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-FR/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="0992d-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0992d-107">Setting</span></span>

<span data-ttu-id="0992d-108">L’action **AtteindreContrôle** possède l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="0992d-108">The **OpenDiagram** action has the following argument.</span></span> 
  
|<span data-ttu-id="0992d-109">**Argument de l’action**</span><span class="sxs-lookup"><span data-stu-id="0992d-109">**Action argument**</span></span>|<span data-ttu-id="0992d-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="0992d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0992d-111">**Nom du contrôle** :</span><span class="sxs-lookup"><span data-stu-id="0992d-111">**Control Name**</span></span> <br/> |<span data-ttu-id="0992d-112">Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus.</span><span class="sxs-lookup"><span data-stu-id="0992d-112">The name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="0992d-113">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0992d-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0992d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0992d-114">Remarks</span></span>

<span data-ttu-id="0992d-115">Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="0992d-115">You can use this method when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="0992d-116">Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="0992d-116">You can also use this method to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="0992d-117">Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.</span><span class="sxs-lookup"><span data-stu-id="0992d-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

