---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341278"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un mécanisme de synchronisation des messages électroniques au lieu d'utiliser l'API de transport. Cette interface est exposée sur un objet Store. En utilisant cette interface et [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir de meilleurs messages d'erreur et de progression que ceux qui apparaissent dans la boîte de dialogue d'envoi/réception dans Microsoft Outlook.
  
La boîte d'envoi se trouve toujours dans la Banque par défaut. Outlook continuera à utiliser les API de transport pour envoyer des messages, car le message sortant ne peut pas se trouver dans le magasin externe.
  
|||
|:-----|:-----|
|Exposé par:  <br/> |Banques et fournisseurs de transport  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Banques et fournisseurs de transport  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implémenté par les fournisseurs de banque de messages. Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

