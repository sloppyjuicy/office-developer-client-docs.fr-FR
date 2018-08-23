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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589083"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit un mécanisme de synchronisation de messagerie au lieu d’utiliser l’API de Transport. Cette interface est exposée sur un objet store. À l’aide de cette interface et [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir une meilleure progression et messages d’erreur que celles qui s’affichent dans la boîte de dialogue d’envoi/réception dans Microsoft Outlook.
  
La boîte d’envoi est toujours dans la banque par défaut. Outlook continuera à utiliser les API de Transport pour envoyer du courrier électronique, car le message sortant ne peut pas être dans le magasin externe.
  
|||
|:-----|:-----|
|Exposés par :  <br/> |Fournisseurs de banque et de transport  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
|Appelée par :  <br/> |Fournisseurs de banque et de Transport  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implémenté par les fournisseurs de banque de messages. Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

