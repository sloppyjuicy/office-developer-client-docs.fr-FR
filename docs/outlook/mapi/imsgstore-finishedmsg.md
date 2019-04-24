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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348761"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au fournisseur de banque de messages d'effectuer un traitement sur un message envoyé. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le traitement du message envoyé a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de banque de messages ne prend pas en charge le traitement des messages envoyés. Cette valeur d'erreur est renvoyée si l'appelant n'est pas le spouleur MAPI.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: FinishedMsg** effectue le traitement sur un message envoyé. Ce traitement peut impliquer la suppression du message, son transfert vers un autre dossier ou les deux actions. Le type de traitement varie selon que les propriétés **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) et **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sont définies ou non. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de **FinishedMsg**, déverrouillez le message identifié par _lpEntryID_ et effectuez le traitement approprié. Le message cible est toujours verrouillé; le spouleur MAPI ne transmet jamais l'identificateur d'entrée d'un message déverrouillé à **FinishedMsg**.
  
Il est possible que ni **PR_DELETE_AFTER_SUBMIT** ni **PR_SENTMAIL_ENTRYID** ne soit défini, que les deux paramètres soient définis ou que l'un ou l'autre soit défini. Le tableau suivant décrit l'action à effectuer en fonction des paramètres: 
  
|||
|:-----|:-----|
|Si aucune des propriétés n'est définie:  <br/> |Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d'envoi).  <br/> |
|Si les deux propriétés sont définies:  <br/> |Déplacez le message dans le dossier indiqué, si vous le souhaitez, puis supprimez-le.  <br/> |
|Si PR_SENTMAIL_ENTRYID est défini:  <br/> |Déplacer le message vers le dossier indiqué.  <br/> |
|Si PR_DELETE_AFTER_SUBMIT est défini:  <br/> |Supprimez le message.  <br/> |
   
Une fois que vous avez pris les mesures appropriées, appelez la méthode [IMAPISupport::D osentmail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

