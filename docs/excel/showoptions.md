---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782191"
---
# <a name="showoptions"></a><span data-ttu-id="4fd66-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="4fd66-103">ShowOptions</span></span>

<span data-ttu-id="4fd66-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4fd66-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4fd66-105">Affiche la boîte de dialogue modale pour collecter des informations à partir de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4fd66-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="4fd66-106">Ce point d’entrée est appelé lorsqu’un utilisateur clique sur le bouton **Options** en regard de la zone **type de Cluster** pour le connecteur de cluster sélectionné dans la boîte de dialogue **Options Excel** (dans la catégorie **Avancé** , dans la section **formules** ).</span><span class="sxs-lookup"><span data-stu-id="4fd66-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="4fd66-107">Connecteurs de cluster sont responsables de leur propre interface de la boîte de dialogue options de mise en œuvre et de stockage des données connexes dans le Registre ou un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="4fd66-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="4fd66-108">Les options sont des utilisateurs internes pour le connecteur de cluster.</span><span class="sxs-lookup"><span data-stu-id="4fd66-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="4fd66-109">Excel n’a pas connaissance d’eux.</span><span class="sxs-lookup"><span data-stu-id="4fd66-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="4fd66-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fd66-110">Parameters</span></span>

<span data-ttu-id="4fd66-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="4fd66-111">_hWndParent_</span></span>
  
> <span data-ttu-id="4fd66-112">Un handle vers la fenêtre Excel.</span><span class="sxs-lookup"><span data-stu-id="4fd66-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fd66-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4fd66-113">Return value</span></span>

<span data-ttu-id="4fd66-114">**xlHpcRetSuccess** si la boîte de dialogue a été affichée ; **xlHpcRetCallFailed** si elle n’était pas affichée.</span><span class="sxs-lookup"><span data-stu-id="4fd66-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4fd66-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="4fd66-115">Remarks</span></span>

<span data-ttu-id="4fd66-116">Connecteurs de cluster peuvent utiliser cette boîte de dialogue pour obtenir des informations, telles que le serveur de cluster à utiliser, à partir de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4fd66-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fd66-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fd66-117">See also</span></span>

- [<span data-ttu-id="4fd66-118">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="4fd66-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

