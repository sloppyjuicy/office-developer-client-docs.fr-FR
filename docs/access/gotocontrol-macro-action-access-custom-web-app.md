---
title: Action de Macro AtteindreContrôle (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Vous pouvez utiliser l’action AtteindreContrôle pour déplacer le focus vers le contrôle spécifié dans l’enregistrement actif de la vue ouverte.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781814"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="626e2-103">Action de Macro AtteindreContrôle (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="626e2-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="626e2-104">Vous pouvez utiliser l’action **AtteindreContrôle** pour déplacer le focus vers le contrôle spécifié dans l’enregistrement actif de la vue ouverte.</span><span class="sxs-lookup"><span data-stu-id="626e2-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="626e2-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="626e2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="626e2-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="626e2-107">Setting</span></span>

<span data-ttu-id="626e2-108">L’action **AtteindreContrôle** possède l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="626e2-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="626e2-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="626e2-109">**Action argument**</span></span>|<span data-ttu-id="626e2-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="626e2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="626e2-111">**Nom du contrôle**</span><span class="sxs-lookup"><span data-stu-id="626e2-111">**Control Name**</span></span> <br/> |<span data-ttu-id="626e2-112">Le nom du champ ou du contrôle où vous voulez l’activer.</span><span class="sxs-lookup"><span data-stu-id="626e2-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="626e2-113">Il s'agit d'un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="626e2-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="626e2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="626e2-114">Remarks</span></span>

<span data-ttu-id="626e2-115">Vous pouvez utiliser cette action lorsque vous souhaitez un champ particulier ou un contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="626e2-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="626e2-116">Vous pouvez également utiliser cette action pour naviguer dans un formulaire en fonction de certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="626e2-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="626e2-117">Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.</span><span class="sxs-lookup"><span data-stu-id="626e2-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

