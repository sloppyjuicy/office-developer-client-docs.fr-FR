---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411413"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="e34dc-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e34dc-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="e34dc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e34dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e34dc-105">Permet aux solutions Microsoft Outlook 2010 et Microsoft Outlook 2013 de savoir si une pièce jointe est considérée comme non sûre et bloquée pour l’affichage et l’indexation.</span><span class="sxs-lookup"><span data-stu-id="e34dc-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e34dc-106">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="e34dc-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e34dc-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="e34dc-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e34dc-108">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="e34dc-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e34dc-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="e34dc-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="e34dc-110">Vérifie si une pièce jointe spécifiée est bloquée par Outlook 2010 ou Outlook 2013 pour l’affichage et l’indexation.</span><span class="sxs-lookup"><span data-stu-id="e34dc-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e34dc-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e34dc-111">Remarks</span></span>

<span data-ttu-id="e34dc-112">Les solutions Outlook 2010 et Outlook 2013 peuvent interroger cette interface pour voir si une pièce jointe est bloquée.</span><span class="sxs-lookup"><span data-stu-id="e34dc-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="e34dc-113">Les pièces jointes bloquées par Outlook 2010 ou Outlook 2013 varient en fonction de la configuration d’Outlook 2010 ou d’Outlook 2013 et des stratégies appliquées par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="e34dc-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e34dc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e34dc-114">See also</span></span>



[<span data-ttu-id="e34dc-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e34dc-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e34dc-116">Vérifier qu’une pièce jointe est bloquée</span><span class="sxs-lookup"><span data-stu-id="e34dc-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

