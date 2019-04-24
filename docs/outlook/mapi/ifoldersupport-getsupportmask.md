---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350833"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="e4cfd-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="e4cfd-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="e4cfd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4cfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4cfd-105">Obtient des informations sur la prise en charge d'un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="e4cfd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4cfd-106">Parameters</span></span>

 <span data-ttu-id="e4cfd-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="e4cfd-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="e4cfd-108">remarquer Masque de masque indiquant si le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="e4cfd-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="e4cfd-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="e4cfd-110">Indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="e4cfd-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="e4cfd-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="e4cfd-112">Indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4cfd-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4cfd-113">Return value</span></span>

<span data-ttu-id="e4cfd-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4cfd-114">S_OK</span></span> 
  
> <span data-ttu-id="e4cfd-115">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-115">The call was successful.</span></span>
    

