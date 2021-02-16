---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411616"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="b5af0-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="b5af0-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="b5af0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5af0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5af0-105">Définit l’ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="b5af0-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b5af0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5af0-106">Parameters</span></span>

 <span data-ttu-id="b5af0-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="b5af0-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="b5af0-108">[in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient l’ordre de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="b5af0-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="b5af0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b5af0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b5af0-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’ordre de tri par défaut est définie.</span><span class="sxs-lookup"><span data-stu-id="b5af0-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="b5af0-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="b5af0-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b5af0-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="b5af0-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="b5af0-113">Le jeu d’ordre de tri par défaut s’applique au dossier indiqué et à tous ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="b5af0-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b5af0-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5af0-114">Return value</span></span>

<span data-ttu-id="b5af0-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5af0-115">S_OK</span></span> 
  
> <span data-ttu-id="b5af0-116">L’ordre de tri a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="b5af0-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="b5af0-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b5af0-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b5af0-118">Le fournisseur de magasins de messages ne prend pas en charge l’enregistrement d’un ordre de tri pour ses tables de contenu de dossiers.</span><span class="sxs-lookup"><span data-stu-id="b5af0-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5af0-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="b5af0-119">Remarks</span></span>

<span data-ttu-id="b5af0-120">La **méthode IMAPIFolder::SaveContentsSort** établit un ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="b5af0-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="b5af0-121">Autrement dit, lorsqu’un client appelle la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier après que le code a appelé **SaveContentsSort,** les lignes de la table des matières retournée apparaissent dans l’ordre établi par **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="b5af0-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="b5af0-122">Tous les fournisseurs de magasins de messages ne sont pas en charge **SaveContentsSort**; Il est acceptable que les fournisseurs de magasins de messages MAPI_E_NO_SUPPORT à partir de la **méthode SaveContentsSort.**</span><span class="sxs-lookup"><span data-stu-id="b5af0-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5af0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5af0-123">See also</span></span>



[<span data-ttu-id="b5af0-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="b5af0-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="b5af0-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b5af0-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="b5af0-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b5af0-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

