---
title: IMAPISync IUnknown
description: IMAPISyncIUnknown fournit un mécanisme de synchronisation des e-mails au lieu d’utiliser l’API transport. Cette interface est exposée sur un objet store.
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
ms.openlocfilehash: 24ecf7a282629f00fc256a12e0f9028528509e3b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827883"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un mécanisme de synchronisation des e-mails au lieu d’utiliser l’API de transport. Cette interface est exposée sur un objet store. En utilisant cette interface et [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir de meilleurs messages de progression et d’erreur que ceux qui apparaissent dans la boîte de dialogue Envoyer/recevoir dans Microsoft Outlook.
  
La boîte de réception se trouve toujours dans le magasin par défaut. Outlook continuez à utiliser les API de transport pour envoyer des messages, car le message sortant ne peut pas se trouver dans le magasin externe.
  
|Propriété|Valeur|
|:-----|:-----|
|Exposé par :  <br/> |Fournisseurs de stockage et de transport  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Fournisseurs de stockage et de transport  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implémenté par les fournisseurs de magasin de messages. Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

