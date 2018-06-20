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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784142"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**S’applique à**: Outlook 
  
Définit ou supprime l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message et gère l’envoi de rapports de lecture.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le paramétrage de la lecture d’un message drapeau, du message MSGFLAG_READ dans sa propriété **PR_MESSAGE_FLAGS** et le traitement des rapports de lecture. Les indicateurs suivants peuvent être définis : 
    
  - CLEAR_READ_FLAG : L’indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé. 
      
  - CLEAR_NRN_PENDING : L’indicateur MSGFLAG_NRN_PENDING doit être désactivée dans **PR_MESSAGE_FLAGS** et un rapport de non-lecture ne doit pas être envoyé. 
      
  - CLEAR_RN_PENDING : L’indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé. 
      
  - GENERATE_RECEIPT_ONLY : Un rapport de lecture doit être envoyé si un est en attente, mais il ne doit y avoir aucune modification de l’état de l’indicateur MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS : Permet de **SetReadFlag** renvoyer avec succès, éventuellement, avant la fin de l’opération. 
      
  - SUPPRESS_RECEIPT : Un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et cet appel remplace l’état du message non lu à lire. Si cet appel ne modifie pas l’état du message, le fournisseur de banque de message peut ignorer cet indicateur.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Indicateur de lecture du message a été configurée ou désactivée.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur de banque de messages ne gère pas la suppression des rapports de lecture.
    
MAPI_E_INVALID_PARAMETER 
  
> Une des combinaisons d’indicateurs suivants est définie dans le paramètre _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::SetReadFlag** définit ou efface l’indicateur MSGFLAG_READ du message dans la propriété **PR_MESSAGE_FLAGS** et les appels [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message. Définition de l’indicateur MSGFLAG_READ marque un message comme ayant été lu, ce qui n’indique pas nécessairement que le destinataire a lu réellement le message. 
  
**SetReadFlags** gère également l’envoi des rapports de lecture. Un rapport de lecture est envoyé uniquement si l’expéditeur a demandé une. 
  
L’indicateur de lecture ne peut pas être modifié pour :
  
- Messages qui n’existent pas.
    
- Les messages qui ont été déplacés vers un autre emplacement.
    
- Messages qui sont ouvertes avec l’autorisation de lecture/écriture.
    
- Messages qui sont actuellement envoyées.
    
## <a name="notes-to-callers"></a>Notes aux appelants

Si aucun des indicateurs sont définies dans le paramètre _ulFlags_ , les règles suivantes s’appliquent : 
  
- Si MSGFLAG_READ est déjà défini, ne faites rien.
    
- Si MSGFLAG_READ n’est pas définie, définissez-la et envoyer les en attente de rapports de lecture si la valeur de la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Si les indicateurs GENERATE_RECEIPT_ONLY et SUPPRESS_RECEIPT sont définies, la PR_READ_RECEIPT_REQUESTED bit, s’il est défini, doit être désactivée et un rapport de lecture ne doit pas être envoyé.
  
Lorsque l’indicateur SUPPRESS_RECEIPT est défini :
  
- Si MSGFLAG_READ est déjà défini, ne faites rien. 
    
- Si MSGFLAG_READ n’est pas définie, définissez-la et annuler les en attente de rapports de lecture.
    
Lorsque l’indicateur CLEAR_READ_FLAG est défini, effacer l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** du chaque message et ne pas envoyer des rapports de lecture. 
  
Lorsque l’indicateur GENERATE_RECEIPT_ONLY est défini, envoyer des rapports de lecture en attente. Ne pas définir ou effacer MSGFLAG_READ.
  
Lorsque les indicateurs GENERATE_RECEIPT_ONLY et SUPPRESS_RECEIPT sont définis, définir la propriété PR_READ_RECEIPT_REQUESTED sur FALSE si elle est définie et ne pas envoyer un rapport de lecture.
  
Vous pouvez optimiser le comportement de rapport en supprimant la génération de rapports de lecture sous certaines conditions. Toutefois, si vous ne prennent pas en charge la suppression des rapports et un client appelle **SetReadFlag** avec l’indicateur SUPPRESS_RECEIPT, retourner MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI utilise la méthode **IMessage::SetReadFlag** pour définir des indicateurs de lecture sur les messages sélectionnés.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage : IMAPIProp](imessageimapiprop.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

