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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783738"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="19f4b-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="19f4b-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="19f4b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19f4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19f4b-105">Définit l’ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="19f4b-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="19f4b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19f4b-106">Parameters</span></span>

 <span data-ttu-id="19f4b-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="19f4b-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="19f4b-108">[in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient l’ordre de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="19f4b-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="19f4b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19f4b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="19f4b-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’ordre de tri par défaut est défini.</span><span class="sxs-lookup"><span data-stu-id="19f4b-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="19f4b-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="19f4b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="19f4b-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="19f4b-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="19f4b-113">L’ensemble d’ordre de tri par défaut s’applique au dossier indiqué et tous ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="19f4b-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19f4b-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="19f4b-114">Return value</span></span>

<span data-ttu-id="19f4b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="19f4b-115">S_OK</span></span> 
  
> <span data-ttu-id="19f4b-116">L’ordre de tri a été enregistré avec succès.</span><span class="sxs-lookup"><span data-stu-id="19f4b-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="19f4b-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="19f4b-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="19f4b-118">Le fournisseur de banque de messages n’autorise pas l’enregistrement d’un ordre de tri pour les tables de son contenu de dossier.</span><span class="sxs-lookup"><span data-stu-id="19f4b-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19f4b-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="19f4b-119">Remarks</span></span>

<span data-ttu-id="19f4b-120">La méthode **IMAPIFolder::SaveContentsSort** établit un ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="19f4b-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="19f4b-121">Autrement dit, lorsqu’un client appelle la méthode de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier après le code appelle **SaveContentsSort**, les lignes dans le tableau renvoyé contenu apparaîtra dans l’ordre établi par **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="19f4b-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="19f4b-122">Prendre en charge tous les fournisseurs de banque de messages **SaveContentsSort**; Il est acceptable pour les fournisseurs de banque de message renvoyer des MAPI_E_NO_SUPPORT à partir de la méthode **SaveContentsSort** .</span><span class="sxs-lookup"><span data-stu-id="19f4b-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19f4b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19f4b-123">See also</span></span>



[<span data-ttu-id="19f4b-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="19f4b-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="19f4b-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="19f4b-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="19f4b-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="19f4b-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

