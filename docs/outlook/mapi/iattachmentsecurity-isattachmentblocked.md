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
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565045"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="260f7-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="260f7-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="260f7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="260f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="260f7-105">Vérifie si une pièce jointe spécifiée est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation.</span><span class="sxs-lookup"><span data-stu-id="260f7-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="260f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="260f7-106">Parameters</span></span>

 <span data-ttu-id="260f7-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="260f7-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="260f7-108">[in] Pointeur vers le nom de fichier d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="260f7-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="260f7-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="260f7-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="260f7-110">[out] Pointeur vers une valeur indiquant **la valeur true** si la pièce jointe spécifiée est bloquée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="260f7-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="260f7-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="260f7-111">See also</span></span>



[<span data-ttu-id="260f7-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="260f7-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="260f7-113">Vérifier qu’une pièce jointe est bloquée</span><span class="sxs-lookup"><span data-stu-id="260f7-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

