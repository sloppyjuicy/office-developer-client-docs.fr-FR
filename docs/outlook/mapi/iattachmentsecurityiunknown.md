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
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326984"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux solutions Microsoft Outlook 2010 et Microsoft Outlook 2013 de déterminer si une pièce jointe est considérée comme non sécurisée et bloquée pour l'affichage et l'indexation.
  
|||
|:-----|:-----|
|Identificateur de l'interface:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Vérifie si une pièce jointe spécifiée est bloquée par Outlook 2010 ou Outlook 2013 pour l'affichage et l'indexation.  <br/> |
   
## <a name="remarks"></a>Remarques

Les solutions Outlook 2010 et Outlook 2013 peuvent interroger cette interface pour déterminer si une pièce jointe est bloquée. Les pièces jointes bloquées par Outlook 2010 ou Outlook 2013 varient en fonction de la configuration d'Outlook 2010 ou d'Outlook 2013, ainsi que des stratégies appliquées par un administrateur.
  
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Vérifier qu'une pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

