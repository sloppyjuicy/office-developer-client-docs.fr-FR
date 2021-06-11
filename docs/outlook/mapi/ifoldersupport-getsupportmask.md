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
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417370"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="a5bb6-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="a5bb6-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="a5bb6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5bb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5bb6-105">Obtient des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="a5bb6-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="a5bb6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a5bb6-106">Parameters</span></span>

 <span data-ttu-id="a5bb6-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="a5bb6-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="a5bb6-108">[out] Masque de bits indiquant si le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="a5bb6-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="a5bb6-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="a5bb6-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="a5bb6-110">Indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="a5bb6-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="a5bb6-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="a5bb6-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="a5bb6-112">Indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="a5bb6-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5bb6-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5bb6-113">Return value</span></span>

<span data-ttu-id="a5bb6-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5bb6-114">S_OK</span></span> 
  
> <span data-ttu-id="a5bb6-115">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5bb6-115">The call was successful.</span></span>
    

