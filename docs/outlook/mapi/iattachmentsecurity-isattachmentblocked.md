---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439778"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="02d7b-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="02d7b-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="02d7b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02d7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02d7b-105">Vérifie si une pièce jointe spécifiée est bloquée par Microsoft Outlook 2010 ou par Microsoft Outlook 2013 pour l'affichage et l'indexation.</span><span class="sxs-lookup"><span data-stu-id="02d7b-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="02d7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02d7b-106">Parameters</span></span>

 <span data-ttu-id="02d7b-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="02d7b-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="02d7b-108">dans Pointeur vers le nom de fichier d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="02d7b-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="02d7b-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="02d7b-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="02d7b-110">remarquer Pointeur vers une valeur indiquant **true** si la pièce jointe spécifiée est bloquée; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="02d7b-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02d7b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02d7b-111">See also</span></span>



[<span data-ttu-id="02d7b-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="02d7b-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="02d7b-113">Vérifier qu'une pièce jointe est bloquée</span><span class="sxs-lookup"><span data-stu-id="02d7b-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

