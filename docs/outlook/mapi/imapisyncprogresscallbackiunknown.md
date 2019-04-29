---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418336"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Transmet le fournisseur Store en tant que champ sur la structure MAPISIB lors d'un appel à [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Le fournisseur de banque d'informations utilise cette interface pour envoyer des commentaires à Microsoft Outlook sur l'état de la synchronisation.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> ||
|Exposé par:  <br/> |Outlook  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Fournisseurs de magasin  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Le fournisseur Store appelle régulièrement cette fonction pour mettre à jour l'État dans la boîte de dialogue d'envoi/réception.  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |Si des erreurs se produisent lors de la synchronisation, le fournisseur de banque d'informations appelle cette fonction pour fournir les détails affichés dans la boîte de dialogue d'envoi/réception.  <br/> |
|[Terminé](imapisyncprogresscallback-done.md) <br/> |Le fournisseur Store appelle cette fonction pour informer Outlook que la synchronisation est terminée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

