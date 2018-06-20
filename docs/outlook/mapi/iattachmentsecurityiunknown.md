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
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**S’applique à**: Outlook 
  
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
  
[Vérifiez la que pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

