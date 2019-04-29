---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424608"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la table de destinataires du message.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le retour de la table. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **GetRecipientTable** de retourner correctement, éventuellement avant que la table soit entièrement disponible pour le client appelant. Si la table n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur. 
    
MAPI_UNICODE 
  
> Les colonnes de chaîne doivent être au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de chaîne doivent être au format ANSI.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers le tableau de destinataires.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de destinataires a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage:: GetRecipientTable** renvoie un pointeur vers la table de destinataires du message, qui inclut des informations sur tous les destinataires du message. Il y a une ligne pour chaque destinataire. 
  
Les tables de destinataires ont un jeu de colonnes différent selon que le message a été envoyé ou non. Pour obtenir la liste complète des colonnes d'un tableau de destinataires, consultez la rubrique [tables](recipient-tables.md)des destinataires.
  
Certaines tables de destinataires prennent en charge un large éventail de restrictions; d'autres non. La prise en charge des restrictions dépend de l'implémentation du fournisseur de banque de messages. 
  
La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants à la table de destinataires: 
  
- [IMAPITable:: QueryColumns](imapitable-querycolumns.md) pour récupérer le jeu de colonnes. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire des lignes. 
    
- [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) pour récupérer l'ordre de tri. 
    
Définition des demandes d'indicateur Unicode pour que les informations de toutes les colonnes de chaînes renvoyées à partir de ces appels soient au format Unicode. Toutefois, étant donné que tous les fournisseurs de banques de messages ne prennent pas en charge Unicode, la définition de cet indicateur n'est qu'une requête.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez modifier une table de destinataires lorsqu'elle est ouverte en appelant la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . **ModifyRecipients** ajoute des destinataires, supprime des destinataires ou modifie les propriétés des destinataires. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

