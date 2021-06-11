---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415774"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="efddf-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="efddf-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="efddf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efddf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efddf-105">Fournit des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="efddf-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efddf-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="efddf-106">Provided by:</span></span>  <br/> |<span data-ttu-id="efddf-107">Fournisseur de magasin de messages</span><span class="sxs-lookup"><span data-stu-id="efddf-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="efddf-108">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="efddf-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="efddf-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="efddf-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="efddf-110">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="efddf-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efddf-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="efddf-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="efddf-112">Obtient des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="efddf-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efddf-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="efddf-113">Remarks</span></span>

<span data-ttu-id="efddf-114">En règle générale, Microsoft Office Outlook un fournisseur de magasin MAPI doit implémenter cette interface si le fournisseur souhaite partager un dossier.</span><span class="sxs-lookup"><span data-stu-id="efddf-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="efddf-115">L’exception est le fournisseur Exchange Server store, qui peut partager des dossiers sans implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="efddf-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="efddf-116">Un client peut interroger **[un IMAPIFolder](imapifolderimapicontainer.md)** pour **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="efddf-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="efddf-117">Si cela réussit, appelez **IFolderSupport::GetSupportMask** et vérifiez la FS_SUPPORTS_SHARING **bit** à définir.</span><span class="sxs-lookup"><span data-stu-id="efddf-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

