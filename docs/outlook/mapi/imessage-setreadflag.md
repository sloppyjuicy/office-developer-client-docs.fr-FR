---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439869"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou efface l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message et gère l'envoi des rapports de lecture.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> dans Masque de réinitialisation des indicateurs qui contrôlent le paramètre de l'indicateur de lecture d'un message qui est l'indicateur MSGFLAG_READ du message dans sa propriété **PR_MESSAGE_FLAGS** et le traitement des rapports de lecture. Les indicateurs suivants peuvent être définis: 
    
  - CLEAR_READ_FLAG: l'indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé. 
      
  - CLEAR_NRN_PENDING: l'indicateur MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de non-lecture ne doit pas être envoyé. 
      
  - CLEAR_RN_PENDING: l'indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé. 
      
  - GENERATE_RECEIPT_ONLY: un rapport de lecture doit être envoyé s'il en est en attente, mais il ne doit y avoir aucune modification dans l'état de l'indicateur MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS: permet à **SetReadFlag** de renvoyer correctement, éventuellement avant la fin de l'opération. 
      
  - SUPPRESS_RECEIPT: un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel change l'état du message de non lu en lecture. Si cet appel ne modifie pas l'état du message, le fournisseur de banque de messages peut ignorer cet indicateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'indicateur de lecture du message a été correctement défini ou désactivé.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur de banque de messages ne prend pas en charge la suppression des rapports lus.
    
MAPI_E_INVALID_PARAMETER 
  
> L'une des combinaisons d'indicateurs suivantes est définie dans le paramètre _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Remarques

La méthode **IMessage:: SetReadFlag** définit ou efface l'indicateur MSGFLAG_READ du message dans la propriété **PR_MESSAGE_FLAGS** et appelle [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) pour enregistrer le message. La définition de l'indicateur MSGFLAG_READ marque un message comme lu, ce qui n'indique pas nécessairement que le destinataire concerné a effectivement lu le message. 
  
**SetReadFlags** gère également l'envoi des rapports de lecture. Un rapport de lecture est envoyé uniquement si l'expéditeur en a demandé un. 
  
L'indicateur de lecture ne peut pas être modifié pour:
  
- Messages qui n'existent pas.
    
- Messages qui ont été déplacés ailleurs.
    
- Messages ouverts avec une autorisation en lecture/écriture.
    
- Messages actuellement envoyés.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si aucun des indicateurs n'est défini dans le paramètre _ulFlags_ , les règles suivantes s'appliquent: 
  
- Si MSGFLAG_READ est déjà défini, ne faites rien.
    
- Si MSGFLAG_READ n'est pas défini, définissez-le et envoyez les rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.
    
Si les deux indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, le bit PR_READ_RECEIPT_REQUESTED, s'il est défini, doit être effacé et un rapport de lecture ne doit pas être envoyé.
  
Lorsque l'indicateur SUPPRESS_RECEIPT est défini:
  
- Si MSGFLAG_READ est déjà défini, ne faites rien. 
    
- Si MSGFLAG_READ n'est pas défini, définissez-le et annulez tous les rapports de lecture en attente.
    
Lorsque l'indicateur CLEAR_READ_FLAG est défini, effacez l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** de chaque message et n'envoyez aucun rapport de lecture. 
  
Lorsque l'indicateur GENERATE_RECEIPT_ONLY est défini, envoyez tous les rapports de lecture en attente. Ne définissez pas MSGFLAG_READ.
  
Lorsque les deux indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, affectez la valeur FALSe à la propriété PR_READ_RECEIPT_REQUESTED si elle est définie et que vous ne souhaitez pas envoyer de rapport de lecture.
  
Vous pouvez optimiser le comportement de rapport en supprimant la génération de rapports en lecture dans certaines conditions. Toutefois, si vous ne prenez pas en charge la suppression des rapports et qu'un client appelle **SetReadFlag** avec l'indicateur SUPPRESS_RECEIPT défini, retournez MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI utilise la méthode **IMessage:: SetReadFlag** pour définir des indicateurs de lecture sur les messages sélectionnés.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage : IMAPIProp](imessageimapiprop.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

