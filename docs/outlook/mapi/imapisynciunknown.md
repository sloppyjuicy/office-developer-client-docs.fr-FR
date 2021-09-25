---
title: IMAPISync IUnknown
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
ms.openlocfilehash: 6df344d6fc63bef9ee475437810e7dbdc290786d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625363"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un mécanisme de synchronisation du courrier électronique au lieu d’utiliser l’API de transport. Cette interface est exposée sur un objet store. En utilisant cette interface et [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir des messages de progression et d’erreur plus importants que ceux qui apparaissent dans la boîte de dialogue Envoyer/Recevoir dans Microsoft Outlook.
  
La boîte d’envoi se trouve toujours dans le magasin par défaut. Outlook continueront d’utiliser les API de transport pour envoyer des messages, car le message sortant ne peut pas se trouver dans le magasin externe.
  
|||
|:-----|:-----|
|Exposé par :  <br/> |Fournisseurs de transport et de magasin  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Fournisseurs de magasins et de transports  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implémenté par les fournisseurs de magasins de messages. Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

