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
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="869ea-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="869ea-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="869ea-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="869ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="869ea-105">Obtient des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="869ea-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="869ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="869ea-106">Parameters</span></span>

 <span data-ttu-id="869ea-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="869ea-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="869ea-108">[out] Masque de bits indiquant si le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="869ea-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="869ea-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="869ea-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="869ea-110">Indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="869ea-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="869ea-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="869ea-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="869ea-112">Indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="869ea-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="869ea-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="869ea-113">Return value</span></span>

<span data-ttu-id="869ea-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="869ea-114">S_OK</span></span> 
  
> <span data-ttu-id="869ea-115">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="869ea-115">The call was successful.</span></span>
    

