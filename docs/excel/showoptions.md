---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310426"
---
# <a name="showoptions"></a><span data-ttu-id="8d96f-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="8d96f-103">ShowOptions</span></span>

<span data-ttu-id="8d96f-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8d96f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8d96f-105">Affiche une boîte de dialogue modale pour collecter des informations auprès de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d96f-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="8d96f-106">Ce point d'entrée est appelé lorsqu'un utilisateur clique sur le bouton **options** en regard de la zone **type de cluster** pour le connecteur de cluster sélectionné dans la boîte de dialogue **Options Excel** (dans la catégorie **avancé** , sous la section **formules** ).</span><span class="sxs-lookup"><span data-stu-id="8d96f-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="8d96f-107">Les connecteurs de cluster sont chargés d'implémenter leur propre interface de boîte de dialogue Options et de stocker les données associées dans le registre ou ailleurs.</span><span class="sxs-lookup"><span data-stu-id="8d96f-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="8d96f-108">Les options sont internes au connecteur de cluster.</span><span class="sxs-lookup"><span data-stu-id="8d96f-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="8d96f-109">Excel ne les prend pas en compte.</span><span class="sxs-lookup"><span data-stu-id="8d96f-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="8d96f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d96f-110">Parameters</span></span>

<span data-ttu-id="8d96f-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="8d96f-111">_hWndParent_</span></span>
  
> <span data-ttu-id="8d96f-112">Handle de la fenêtre Excel.</span><span class="sxs-lookup"><span data-stu-id="8d96f-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d96f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d96f-113">Return value</span></span>

<span data-ttu-id="8d96f-114">**xlHpcRetSuccess** si la boîte de dialogue a été affichée; **xlHpcRetCallFailed** si elle n'a pas été affichée.</span><span class="sxs-lookup"><span data-stu-id="8d96f-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d96f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d96f-115">Remarks</span></span>

<span data-ttu-id="8d96f-116">Les connecteurs de cluster peuvent utiliser cette boîte de dialogue pour obtenir des informations, telles que le serveur de cluster à utiliser, de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d96f-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d96f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d96f-117">See also</span></span>

- [<span data-ttu-id="8d96f-118">Fonctions du connecteur de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="8d96f-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

