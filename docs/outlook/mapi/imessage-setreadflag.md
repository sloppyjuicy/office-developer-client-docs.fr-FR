---
title: IMessageSetReadFlag
description: IMessageSetReadFlag définit ou efface l’indicateur MSGFLAG_READ dans la propriété PR_MESSAGE_FLAGS du message et gère l’envoi de rapports de lecture.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
ms.openlocfilehash: 461b7b98c5daab52009599e74df510f7f533f98d
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826938"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou efface l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message et gère l’envoi de rapports de lecture.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent le paramètre de l’indicateur de lecture d’un message, c’est-à-dire l’indicateur MSGFLAG_READ du message dans sa propriété **PR_MESSAGE_FLAGS** et le traitement des rapports de lecture. Les indicateurs suivants peuvent être définis : 
    
  - CLEAR_READ_FLAG : l’indicateur de MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé. 
      
  - CLEAR_NRN_PENDING : l’indicateur de MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport non lu ne doit pas être envoyé. 
      
  - CLEAR_RN_PENDING : l’indicateur de MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé. 
      
  - GENERATE_RECEIPT_ONLY : un rapport de lecture doit être envoyé si un rapport est en attente, mais il ne doit pas y avoir de modification de l’état de l’indicateur MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS : permet à **SetReadFlag** de retourner correctement, éventuellement avant la fin de l’opération. 
      
  - SUPPRESS_RECEIPT : un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel modifie l’état du message de non lu à lire. Si cet appel ne modifie pas l’état du message, le fournisseur du magasin de messages peut ignorer cet indicateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’indicateur de lecture du message a été correctement défini ou effacé.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur du magasin de messages ne prend pas en charge la suppression des rapports de lecture.
    
MAPI_E_INVALID_PARAMETER 
  
> L’une des combinaisons d’indicateurs suivantes est définie dans le paramètre _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::SetReadFlag** définit ou efface l’indicateur de MSGFLAG_READ du message dans la propriété **PR_MESSAGE_FLAGS** et appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message. La définition de l’indicateur MSGFLAG_READ marque un message comme ayant été lu, ce qui n’indique pas nécessairement que le destinataire prévu a réellement lu le message. 
  
**SetReadFlags** gère également l’envoi de rapports en lecture. Un rapport de lecture n’est envoyé que si l’expéditeur en a demandé un. 
  
L’indicateur de lecture ne peut pas être modifié pour :
  
- Messages qui n’existent pas.
    
- Messages déplacés ailleurs.
    
- Messages ouverts avec autorisation de lecture/écriture.
    
- Messages actuellement envoyés.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si aucun des indicateurs n’est défini dans le paramètre _ulFlags_ , les règles suivantes s’appliquent : 
  
- Si MSGFLAG_READ est déjà défini, ne faites rien.
    
- Si MSGFLAG_READ n’est pas défini, définissez-le et envoyez des rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.
    
Si les indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, le bit PR_READ_RECEIPT_REQUESTED, s’il est défini, doit être effacé et un rapport de lecture ne doit pas être envoyé.
  
Lorsque l’indicateur SUPPRESS_RECEIPT est défini :
  
- Si MSGFLAG_READ est déjà défini, ne faites rien. 
    
- Si MSGFLAG_READ n’est pas défini, définissez-le et annulez les rapports de lecture en attente.
    
Lorsque l’indicateur CLEAR_READ_FLAG est défini, effacez l’indicateur de MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** de chaque message et n’envoyez aucun rapport de lecture. 
  
Lorsque l’indicateur GENERATE_RECEIPT_ONLY est défini, envoyez tous les rapports en lecture en attente. Ne définissez pas ou n’effacez pas MSGFLAG_READ.
  
Lorsque les indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, définissez la propriété PR_READ_RECEIPT_REQUESTED sur FALSE si elle est définie et n’envoyez pas de rapport de lecture.
  
Vous pouvez optimiser le comportement des rapports en supprimant la génération de rapports en lecture dans certaines conditions. Toutefois, si vous ne prenez pas en charge la suppression des rapports et qu’un client appelle **SetReadFlag** avec l’indicateur SUPPRESS_RECEIPT défini, retournez MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI utilise la méthode **IMessage::SetReadFlag** pour définir des indicateurs de lecture sur les messages sélectionnés. |
   
## <a name="see-also"></a>Voir aussi

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage : IMAPIProp](imessageimapiprop.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

