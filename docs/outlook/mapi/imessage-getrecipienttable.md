---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 466e0e8d5adee88b8e6a7d1b70c79bf075310cb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610509"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la table des destinataires du message.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le retour de la table. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **GetRecipientTable** de renvoyer correctement, éventuellement avant que la table soit entièrement disponible pour le client appelant. Si la table n’est pas disponible, un appel ultérieur à celui-ci peut provoquer une erreur. 
    
MAPI_UNICODE 
  
> Les colonnes de chaîne doivent être au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les colonnes de chaîne doivent être au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau des destinataires.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table des destinataires a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMessage::GetRecipientTable** renvoie un pointeur vers la table des destinataires du message, qui inclut des informations sur tous les destinataires du message. Il existe une ligne pour chaque destinataire. 
  
Les tables des destinataires ont un ensemble de colonnes différent selon que le message a été envoyé ou non. Pour obtenir la liste complète des colonnes d’une table des destinataires, voir [Tables des destinataires.](recipient-tables.md)
  
Certaines tables de destinataires supportent un large éventail de restrictions . d’autres non. La prise en charge des restrictions dépend de l’implémentation du fournisseur de magasins de messages. 
  
La définition MAPI_UNICODE’indicateur dans le  _paramètre ulFlags_ affecte les appels suivants à la table des destinataires : 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) pour récupérer le jeu de colonnes. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri. 
    
La définition de l’indicateur Unicode demande que les informations des colonnes de chaîne renvoyées par ces appels soient au format Unicode. Toutefois, étant donné que tous les fournisseurs de banque de messages ne sont pas en charge Unicode, la définition de cet indicateur n’est qu’une demande.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez modifier une table des destinataires lorsqu’elle est ouverte en appelant la méthode [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) **ModifyRecipients** ajoute des destinataires, supprime des destinataires ou modifie les propriétés des destinataires. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

