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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567852"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="d7b1a-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="d7b1a-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="d7b1a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7b1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7b1a-105">Obtient des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="d7b1a-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="d7b1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7b1a-106">Parameters</span></span>

 <span data-ttu-id="d7b1a-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="d7b1a-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="d7b1a-108">[out] Masque de bits indiquant si le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="d7b1a-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="d7b1a-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="d7b1a-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="d7b1a-110">Indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="d7b1a-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="d7b1a-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="d7b1a-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="d7b1a-112">Indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="d7b1a-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7b1a-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7b1a-113">Return value</span></span>

<span data-ttu-id="d7b1a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7b1a-114">S_OK</span></span> 
  
> <span data-ttu-id="d7b1a-115">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="d7b1a-115">The call was successful.</span></span>
    

