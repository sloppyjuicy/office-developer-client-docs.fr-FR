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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564170"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="8d1f8-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d1f8-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="8d1f8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d1f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d1f8-105">Fournit des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="8d1f8-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d1f8-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="8d1f8-106">Provided by:</span></span>  <br/> |<span data-ttu-id="8d1f8-107">Fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="8d1f8-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="8d1f8-108">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="8d1f8-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8d1f8-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="8d1f8-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8d1f8-110">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="8d1f8-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d1f8-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="8d1f8-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="8d1f8-112">Obtient des informations sur la prise en charge d’un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="8d1f8-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d1f8-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d1f8-113">Remarks</span></span>

<span data-ttu-id="8d1f8-114">En règle générale, Microsoft Office Outlook requiert une MAPI magasin du fournisseur pour implémenter cette interface si le fournisseur souhaite partager un dossier.</span><span class="sxs-lookup"><span data-stu-id="8d1f8-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="8d1f8-115">L’exception est le fournisseur de banque Exchange Server, qui peut partager des dossiers sans implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="8d1f8-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="8d1f8-116">Un client peut demander un **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="8d1f8-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="8d1f8-117">Si cette tentative réussit, appelez **IFolderSupport::GetSupportMask** et vérifiez le bit **FS_SUPPORTS_SHARING** à définir.</span><span class="sxs-lookup"><span data-stu-id="8d1f8-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

