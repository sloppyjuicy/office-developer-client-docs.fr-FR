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
ms.openlocfilehash: fe722e8723fdc3868cbbc3188f03e13ef3f466f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575335"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table sortant de la file d’attente, une table qui comporte des informations sur tous les messages en file d’attente sortante de la banque de messages. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau sortant de la file d’attente.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le tableau sortant de la file d’attente a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::GetOutgoingQueue** fournit le spouleur MAPI d’accéder à la table qui affiche la file d’attente de la banque de messages de messages sortants. En règle générale, les messages sont placés dans le tableau de file d’attente sortant après que leur méthode [IMessage::SubmitMessage](imessage-submitmessage.md) est appelée. Toutefois, étant donné que l’ordre de soumission affecte l’ordre d’envoi pour le fournisseur de transport et de prétraitement, certains messages qui ont été marquées pour l’envoi n’apparaîtront dans la table de file d’attente sortant immédiatement. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Pour obtenir la liste des propriétés qui doit être inclus en tant que colonnes dans votre tableau de file d’attente sortant, voir [Les Tables de file d’attente sortante](outgoing-queue-tables.md). 
  
Étant donné que le spouleur MAPI est conçu pour accepter les messages provenant d’une banque de messages dans l’ordre croissant de l’heure d’envoi, soit autoriser le spouleur MAPI trier le tableau sortant de la file d’attente pour correspondre à cette commande ou comme l’ordre de tri par défaut.
  
À prendre en charge les notifications de la table de file d’attente de messages sortants, en vous assurant que le spouleur MAPI est averti lorsque le contenu de la file d’attente change. 
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

