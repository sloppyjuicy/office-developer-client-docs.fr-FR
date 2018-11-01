---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589951"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active le fournisseur de banque de messages effectuer le traitement sur un message envoyé. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Traitement sur le message envoyé a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de banque de messages ne gère pas le traitement du message envoyé. Cette valeur d’erreur est renvoyée si l’appelant n’est pas le spouleur MAPI.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::FinishedMsg** effectue un traitement dans un message envoyé. Ce traitement peut impliquer la suppression du message, son déplacement vers un autre dossier, ou les deux actions. Le type de traitement dépend si les **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) et les propriétés de **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sont définies. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Dans votre implémentation de **FinishedMsg**, déverrouiller le message identifié par _lpEntryID_ et effectuer le traitement approprié. Le message cible doit toujours être verrouillé ; le spouleur MAPI passe jamais l’identificateur d’entrée pour un message déverrouillé à **FinishedMsg**.
  
Il est possible que **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** est définie, les deux sont définies, ni une ou l’autre est défini. Le tableau suivant décrit l’action que vous devez prendre en fonction des paramètres : 
  
|||
|:-----|:-----|
|Si aucune propriété n’est définie :  <br/> |Laissez le message dans le dossier à partir de laquelle il a été envoyé (généralement la boîte d’envoi).  <br/> |
|Si les deux propriétés sont définies :  <br/> |Déplacer le message vers le dossier indiqué, si vous le souhaitez, puis supprimez-le.  <br/> |
|Si PR_SENTMAIL_ENTRYID est défini :  <br/> |Déplacer le message vers le dossier indiqué.  <br/> |
|Si PR_DELETE_AFTER_SUBMIT est défini :  <br/> |Supprimer le message.  <br/> |
   
Après avoir mis quelque action est appropriée, appelez la méthode de [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

