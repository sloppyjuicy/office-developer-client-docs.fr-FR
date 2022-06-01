---
title: IAttachmentSecurity IUnknown
description: Permet aux solutions Microsoft Outlook 2010 et Microsoft Outlook 2013 de déterminer si une pièce jointe est considérée comme non sécurisée et bloquée pour l’affichage et l’indexation.
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
ms.openlocfilehash: 2d8736b2f555cc8e90935e3bc01021374372e480
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812312"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux solutions Microsoft Outlook 2010 et Microsoft Outlook 2013 de déterminer si une pièce jointe est considérée comme non sécurisée et bloquée pour l’affichage et l’indexation.
  
|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’interface :  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Vérifie si une pièce jointe spécifiée est bloquée par Outlook 2010 ou Outlook 2013 pour l’affichage et l’indexation. |
   
## <a name="remarks"></a>Remarques

Outlook solutions 2010 et Outlook 2013 peuvent interroger cette interface pour voir si une pièce jointe est bloquée. Les pièces jointes bloquées par Outlook 2010 ou Outlook 2013 varient selon la façon dont Outlook 2010 ou Outlook 2013 a été configuré et les stratégies appliquées par un administrateur.
  
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Vérifier qu’une pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

