---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f20f891df60495407609653831e2442c9167dec2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592465"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux Microsoft Outlook 2010 et Microsoft Outlook 2013 de savoir si une pièce jointe est considérée comme non sûre et bloquée pour l’affichage et l’indexation.
  
|||
|:-----|:-----|
|Identificateur d’interface :  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Vérifie si une pièce jointe spécifiée est bloquée par Outlook 2010 ou Outlook 2013 pour l’affichage et l’indexation.  <br/> |
   
## <a name="remarks"></a>Remarques

Outlook solutions 2010 et Outlook 2013 peuvent interroger cette interface pour voir si une pièce jointe est bloquée. Les pièces jointes bloquées par Outlook 2010 ou Outlook 2013 varient en fonction de la configuration de Outlook 2010 ou Outlook 2013 et des stratégies appliquées par un administrateur.
  
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Vérifier qu’une pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

