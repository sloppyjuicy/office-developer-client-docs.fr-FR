---
title: IMsgStoreFinishedMsg
description: IMsgStore FinishedMsg permet au fournisseur de magasin de messages d’effectuer le traitement sur un message envoyé. Il est appelé uniquement par le spouleur MAPI.
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
ms.openlocfilehash: d1f48aa15e8a51d539cc56e404318df6e6b0c1d1
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828163"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au fournisseur du magasin de messages d’effectuer le traitement sur un message envoyé. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le traitement du message envoyé a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur du magasin de messages ne prend pas en charge le traitement des messages envoyés. Cette valeur d’erreur est retournée si l’appelant n’est pas le spouleur MAPI.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::FinishedMsg** effectue le traitement sur un message envoyé. Ce traitement peut impliquer la suppression du message, son déplacement vers un autre dossier ou les deux actions. Le type de traitement dépend de la définition des propriétés **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) et **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de **FinishedMsg**, déverrouillez le message identifié par  _lpEntryID_ et effectuez le traitement approprié. Le message cible est toujours verrouillé ; le spouleur MAPI ne transmet jamais l’identificateur d’entrée d’un message déverrouillé à **FinishedMsg**.
  
Il est possible qu’aucun **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** n’est défini, que les deux soient définis ou que l’un ou l’autre n’est défini. Le tableau suivant décrit l’action que vous devez effectuer en fonction des paramètres : 
  
|Propriété|Valeur|
|:-----|:-----|
|Si aucune des propriétés n’est définie :  <br/> |Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d’envoi). |
|Si les deux propriétés sont définies :  <br/> |Déplacez le message vers le dossier indiqué, le cas échéant, puis supprimez-le. |
|Si PR_SENTMAIL_ENTRYID est défini :  <br/> |Déplacez le message vers le dossier indiqué. |
|Si PR_DELETE_AFTER_SUBMIT est défini :  <br/> |Supprimez le message. |
   
Une fois que vous avez pris l’action appropriée, appelez la méthode [IMAPISupport::D oSentMail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

