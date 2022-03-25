---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ed59f371c3dc7d0a1d9b1c33509203f730e3e9bc
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781095"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au fournisseur de magasin de messages d’effectuer un traitement sur un message envoyé. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le traitement sur le message envoyé a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de la boutique de messages ne prend pas en charge le traitement des messages envoyés. Cette valeur d’erreur est renvoyée si l’appelant n’est pas lepooler MAPI.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::FinishedMsg** effectue un traitement sur un message envoyé. Ce traitement peut impliquer la suppression du message, son déplacement vers un autre dossier ou les deux actions. Le type de traitement varie selon que les propriétés **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) et **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sont définies. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de **FinishedMsg**, déverrouillez le message identifié par  _lpEntryID_ et effectuez le traitement approprié. Le message cible est toujours verrouillé . Lepooler MAPI ne transmet jamais l’identificateur d’entrée d’un message déverrouillé à **FinishedMsg**.
  
Il est possible qu’aucun **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** ne soit définie, que les deux soient définies ou que l’une ou l’autre soit définie. Le tableau suivant décrit l’action que vous devez prendre en fonction des paramètres : 
  
|Propriété|Valeur|
|:-----|:-----|
|Si aucune des propriétés n’est définie :  <br/> |Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d’envoi). |
|Si les deux propriétés sont définies :  <br/> |Déplacez le message dans le dossier indiqué, si vous le souhaitez, puis supprimez-le. |
|Si PR_SENTMAIL_ENTRYID est définie :  <br/> |Déplacez le message vers le dossier indiqué. |
|Si PR_DELETE_AFTER_SUBMIT est définie :  <br/> |Supprimez le message. |
   
Une fois que vous avez pris les mesures appropriées, appelez la méthode [IMAPISupport::D oSentMail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

