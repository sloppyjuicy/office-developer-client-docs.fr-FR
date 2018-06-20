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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783637"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="adf1e-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="adf1e-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="adf1e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="adf1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="adf1e-105">Autorise les solutions Microsoft Outlook 2010 et Microsoft Outlook 2013 permettant de savoir si une pièce jointe est considéré comme non sécurisés et bloqués pour l’affichage et l’indexation.</span><span class="sxs-lookup"><span data-stu-id="adf1e-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adf1e-106">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="adf1e-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="adf1e-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="adf1e-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="adf1e-108">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="adf1e-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="adf1e-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="adf1e-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="adf1e-110">Vérifie si une pièce jointe spécifiée est bloquée par Outlook 2010 ou Outlook 2013 pour l’affichage et l’indexation.</span><span class="sxs-lookup"><span data-stu-id="adf1e-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adf1e-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="adf1e-111">Remarks</span></span>

<span data-ttu-id="adf1e-112">Solutions Outlook 2010 et Outlook 2013 peuvent interroger cette interface pour voir si une pièce jointe est bloquée.</span><span class="sxs-lookup"><span data-stu-id="adf1e-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="adf1e-113">Les pièces jointes bloquées par Outlook 2010 ou Outlook 2013 varient selon la façon dont Outlook 2010 ou Outlook 2013 a été configuré et les stratégies qu’un administrateur a appliqué.</span><span class="sxs-lookup"><span data-stu-id="adf1e-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="adf1e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adf1e-114">See also</span></span>



[<span data-ttu-id="adf1e-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="adf1e-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="adf1e-116">Vérifiez la que pièce jointe est bloquée</span><span class="sxs-lookup"><span data-stu-id="adf1e-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

