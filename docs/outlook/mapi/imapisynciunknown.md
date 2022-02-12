---
title: IMAPISync  IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e459f0137a005ca9c8011144153224ac5c447e6
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772076"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un mécanisme de synchronisation du courrier électronique au lieu d’utiliser l’API de transport. Cette interface est exposée sur un objet store. À l’aide de cette interface et [d’IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir des messages d’erreur et de progression meilleurs que ceux qui apparaissent dans la boîte de dialogue Envoyer/Recevoir dans Microsoft Outlook.
  
La boîte d’envoi se trouve toujours dans le magasin par défaut. Outlook continuer à utiliser les API de transport pour envoyer des messages, car le message sortant ne peut pas se trouver dans le magasin externe.
  
|||
|:-----|:-----|
|Exposé par :  <br/> |Fournisseurs de transport et de magasin  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Fournisseurs de magasins et de transports  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implémenté par les fournisseurs de magasins de messages. Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

