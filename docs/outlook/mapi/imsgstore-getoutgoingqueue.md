---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434150"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table de files d’attente sortante, une table qui contient des informations sur tous les messages de la file d’attente sortante de la boutique de messages. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de files d’attente sortantes.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table des files d’attente sortantes a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::GetOutgoingQueue** permet aupooler MAPI d’accéder à la table qui affiche la file d’attente des messages sortants de la boutique de messages. En règle générale, les messages sont placés dans la table des files d’attente sortantes après l’appel de leur méthode [IMessage::SubmitMessage.](imessage-submitmessage.md) Toutefois, étant donné que l’ordre d’envoi affecte l’ordre de prétraitation et d’envoi au fournisseur de transport, certains messages marqués pour l’envoi peuvent ne pas apparaître immédiatement dans la table des files d’attente sortantes. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Pour obtenir la liste des propriétés qui doivent être incluses en tant que colonnes dans votre table de file d’attente sortante, voir Tables de files [d’attente sortantes.](outgoing-queue-tables.md) 
  
Étant donné que lepooler MAPI est conçu pour accepter les messages provenant d’une boutique de messages dans l’ordre croissant du temps d’envoi, autorisez lepoolur MAPI à trier la table des files d’attente sortantes pour qu’elle corresponde à cet ordre ou établissez-la en tant qu’ordre de tri par défaut.
  
Vous devez prendre en charge les notifications pour la table des files d’attente des messages sortants, en vous assurant que lepooler MAPI est averti lorsque le contenu de la file d’attente change. 
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

