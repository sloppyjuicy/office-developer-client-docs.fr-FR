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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f182610f9cf4874cc18c409960e1f8b23f853d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574825"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Autorise les solutions Microsoft Outlook 2010 et Microsoft Outlook 2013 permettant de savoir si une pièce jointe est considéré comme non sécurisés et bloqués pour l’affichage et l’indexation.
  
|||
|:-----|:-----|
|Identificateur de l’interface :  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Vérifie si une pièce jointe spécifiée est bloquée par Outlook 2010 ou Outlook 2013 pour l’affichage et l’indexation.  <br/> |
   
## <a name="remarks"></a>Remarques

Solutions Outlook 2010 et Outlook 2013 peuvent interroger cette interface pour voir si une pièce jointe est bloquée. Les pièces jointes bloquées par Outlook 2010 ou Outlook 2013 varient selon la façon dont Outlook 2010 ou Outlook 2013 a été configuré et les stratégies qu’un administrateur a appliqué.
  
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Vérifier qu’une pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

