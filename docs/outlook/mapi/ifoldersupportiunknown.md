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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351386"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="563a7-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="563a7-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="563a7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="563a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="563a7-105">Fournit des informations sur la prise en charge du partage par un dossier.</span><span class="sxs-lookup"><span data-stu-id="563a7-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="563a7-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="563a7-106">Provided by:</span></span>  <br/> |<span data-ttu-id="563a7-107">Fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="563a7-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="563a7-108">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="563a7-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="563a7-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="563a7-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="563a7-110">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="563a7-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="563a7-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="563a7-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="563a7-112">Obtient des informations sur la prise en charge d'un dossier pour le partage.</span><span class="sxs-lookup"><span data-stu-id="563a7-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="563a7-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="563a7-113">Remarks</span></span>

<span data-ttu-id="563a7-114">En règle générale, Microsoft Office Outlook requiert un fournisseur de banque MAPI pour implémenter cette interface si le fournisseur souhaite partager un dossier.</span><span class="sxs-lookup"><span data-stu-id="563a7-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="563a7-115">L'exception est le fournisseur de banque d'Exchange Server, qui peut partager des dossiers sans mettre en œuvre cette interface.</span><span class="sxs-lookup"><span data-stu-id="563a7-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="563a7-116">Un client peut interroger un **[IMAPIFolder](imapifolderimapicontainer.md)** pour **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="563a7-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="563a7-117">Si cette opération réussit, appelez **IFolderSupport:: GetSupportMask** et vérifiez que le bit **FS_SUPPORTS_SHARING** doit être défini.</span><span class="sxs-lookup"><span data-stu-id="563a7-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

