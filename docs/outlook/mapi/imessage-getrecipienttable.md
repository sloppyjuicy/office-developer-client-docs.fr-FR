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
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579535"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie un tableau de destinataire du message.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le retour de la table. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet de **GetRecipientTable** renvoyer avec succès, éventuellement, avant de la table est totalement disponible au client appelant. Si le tableau n’est pas disponible, vous appelez suivante lui peut provoquer une erreur. 
    
MAPI_UNICODE 
  
> Colonnes de la chaîne doivent être au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de la chaîne doivent être au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de destinataires.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La table de destinataires a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::GetRecipientTable** retourne un pointeur vers la table des destinataires du message, qui consacrée des informations sur tous les destinataires du message. Il existe une ligne pour chaque destinataire. 
  
Tables de destinataires ont une colonne différente selon que le message a été envoyé. Pour obtenir une liste complète des colonnes dans une table de destinataires, voir [Les Tables de destinataire](recipient-tables.md).
  
Certaines tables de destinataires de prendre en charge une grande variété de restrictions ; d’autres ne le sont pas. Prise en charge des restrictions dépend de l’implémentation du fournisseur de banque de messages. 
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants de la table de destinataires : 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) pour extraire l’ensemble de colonnes. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri. 
    
Si les demandes d’indicateur Unicode que les informations des colonnes de la chaîne retournée par ces appels au format Unicode. Toutefois, étant donné que tous les fournisseurs de banque de messages prennent en charge Unicode, définition de cet indicateur est uniquement une demande.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez modifier une table de destinataires lorsqu’il est ouvert en appelant la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . **ModifyRecipients** ajoute des destinataires, supprime les destinataires ou modifie les propriétés de destinataire. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

