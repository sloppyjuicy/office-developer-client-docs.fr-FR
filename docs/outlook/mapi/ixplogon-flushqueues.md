---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784500"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**S’applique à**: Outlook 
  
Demande que le fournisseur de transport remettre immédiatement tous les messages entrants ou sortants en attente.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.
    
 _cbTargetTransport_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpTargetTransport_
  
> [in] Réservé ; doit être NULL.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle comment la purge des messages en file d’attente est effectué. Les indicateurs suivants peuvent être définis :
    
FLUSH_DOWNLOAD 
  
> La file d’attente de messages entrants ou les files d’attente doivent être vidés.
    
FLUSH_FORCE 
  
> Le fournisseur de transport doit traiter cette demande, si possible, même si cela n’est beaucoup de temps. 
    
FLUSH_NO_UI 
  
> Le fournisseur de transport ne doit pas afficher une interface utilisateur.
    
FLUSH_UPLOAD 
  
> La file d’attente de messages sortants ou les files d’attente doivent être vidés.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::FlushQueues** pour conseiller le fournisseur de transport que le spouleur MAPI est sur le point de commencer le traitement des messages. Le fournisseur de transport doit appeler la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour définir un bit approprié pour son état dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état. Après la mise à jour de la ligne d’état, le fournisseur de transport doit renvoyer S_OK pour l’appel de **FlushQueues** . Le spouleur MAPI démarre ensuite l’envoi des messages, l’opération en cours synchrone pour le spouleur MAPI. 
  
Pour prendre en charge son implémentation de la méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , le spouleur MAPI appelle **IXPLogon::FlushQueues** pour tous les objets d’ouverture de session pour les fournisseurs de transport actif qui sont en cours d’exécution dans une session de profil. Lorsque la méthode de **FlushQueues** d’un fournisseur de transport est appelée à la suite d’une application cliente appelle à **IMAPIStatus::FlushQueues**, le traitement du message se produit en mode asynchrone au client.
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

