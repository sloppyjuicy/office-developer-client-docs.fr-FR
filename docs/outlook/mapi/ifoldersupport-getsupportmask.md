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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783682"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="9b5f0-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="9b5f0-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="9b5f0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b5f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b5f0-105">Obtient des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="9b5f0-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="9b5f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b5f0-106">Parameters</span></span>

 <span data-ttu-id="9b5f0-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="9b5f0-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="9b5f0-108">[out] Masque de bits indiquant si le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="9b5f0-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="9b5f0-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="9b5f0-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="9b5f0-110">Indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="9b5f0-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="9b5f0-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="9b5f0-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="9b5f0-112">Indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="9b5f0-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b5f0-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9b5f0-113">Return value</span></span>

<span data-ttu-id="9b5f0-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b5f0-114">S_OK</span></span> 
  
> <span data-ttu-id="9b5f0-115">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="9b5f0-115">The call was successful.</span></span>
    

