---
title: Déclenchererreur, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: L'action Déclenchererreur affiche une fenêtre contextuelle qui contient un message d'erreur spécifié.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408242"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="f9926-103">Déclenchererreur, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="f9926-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f9926-104">L'action **déclenchererreur** affiche une fenêtre contextuelle qui contient un message d'erreur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9926-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f9926-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f9926-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f9926-107">L’action **DéclencherErreur** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="f9926-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f9926-108">Setting</span><span class="sxs-lookup"><span data-stu-id="f9926-108">Setting</span></span>

<span data-ttu-id="f9926-109">L'action **déclenchererreur** possède l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="f9926-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="f9926-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="f9926-110">**Argument**</span></span>|<span data-ttu-id="f9926-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9926-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f9926-112">_Description de l’erreur_</span><span class="sxs-lookup"><span data-stu-id="f9926-112">_Error Description_</span></span> <br/> |<span data-ttu-id="f9926-113">Expression de type Chaîne qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9926-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9926-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9926-114">Remarks</span></span>

<span data-ttu-id="f9926-115">Lorsque l'action **déclenchererreur** est appelée, toutes les opérations de la transaction en cours sont annulées.</span><span class="sxs-lookup"><span data-stu-id="f9926-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

