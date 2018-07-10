---
title: Action de Macro Déclenchererreur (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: L’action Déclenchererreur affiche une fenêtre contenant un message d’erreur spécifié.
ms.openlocfilehash: 1176804106c5cfd9d4bd30f79f47975593089dbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781967"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="ed566-103">Action de Macro Déclenchererreur (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="ed566-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ed566-104">L’action **Déclenchererreur** affiche une fenêtre contenant un message d’erreur spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed566-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ed566-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ed566-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ed566-107">L'action **DéclencherErreur** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="ed566-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ed566-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ed566-108">Setting</span></span>

<span data-ttu-id="ed566-109">L’action **Déclenchererreur** possède l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="ed566-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="ed566-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="ed566-110">**Argument**</span></span>|<span data-ttu-id="ed566-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ed566-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ed566-112">_Description de l’erreur_</span><span class="sxs-lookup"><span data-stu-id="ed566-112">_Error Description_</span></span> <br/> |<span data-ttu-id="ed566-113">Expression de type Chaîne qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed566-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed566-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ed566-114">Remarks</span></span>

<span data-ttu-id="ed566-115">Lorsque l’action **Déclenchererreur** est appelée, toutes les opérations dans la transaction en cours sont annulées.</span><span class="sxs-lookup"><span data-stu-id="ed566-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

