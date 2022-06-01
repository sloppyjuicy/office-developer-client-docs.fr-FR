---
title: IMAPIFolderSetReadFlags
description: IMAPIFolderSetReadFlags définit ou efface l’indicateur de MSGFLAG_READ dans la propriété PR_MESSAGE_FLAGS d’un ou plusieurs messages du dossier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
ms.openlocfilehash: e3a2799d7ca82ca9b2bcbc760f8a36244f6a0c9c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816170"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou efface l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier, et gère l’envoi de rapports de lecture. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_lpMsgList_
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le message ou les messages qui ont des indicateurs de lecture à définir ou à effacer. Si  _lpMsgList_ a la valeur NULL, les indicateurs de lecture de tous les messages du dossier sont définis ou effacés. 
    
_ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
_lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur MESSAGE_DIALOG est défini dans  _ulFlags_.
    
_ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le paramètre de l’indicateur de lecture d’un message et le traitement des rapports de lecture. Les indicateurs suivants peuvent être définis :
    
  - CLEAR_READ_FLAG : l’indicateur de MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé. 
        
  - CLEAR_NRN_PENDING : L’indicateur de MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport non lu ne doit pas être envoyé. 
        
  - CLEAR_RN_PENDING : l’indicateur de MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé. 
        
  - GENERATE_RECEIPT_ONLY : un rapport de lecture doit être envoyé si un rapport est en attente, mais il ne doit pas y avoir de modification de l’état de l’indicateur MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS : permet à **SetReadFlags** de retourner correctement, éventuellement avant la fin de l’opération. 
        
  - MESSAGE_DIALOG : affiche un indicateur de progression pendant que l’opération se poursuit.
    
  - SUPPRESS_RECEIPT : un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel modifie l’état du message de non lu à lire. Si cet appel ne modifie pas l’état du message, le fournisseur du magasin de messages peut ignorer cet indicateur.
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
> L’indicateur de lecture du ou des messages spécifiés a été correctement défini ou effacé.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur du magasin de messages ne prend pas en charge la suppression des rapports de lecture.
    
MAPI_E_INVALID_PARAMETER 
  
> L’une des combinaisons incompatibles suivantes d’indicateurs est définie dans le paramètre _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais tous les messages n’ont pas été traités avec succès. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::SetReadFlags** définit ou efface l’indicateur de MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** d’un ou de plusieurs messages du dossier. La définition de l’indicateur MSGFLAG_READ marque un message comme lu, ce qui n’indique pas nécessairement que le destinataire prévu a réellement lu le message. 
  
**SetReadFlags** gère également l’envoi de rapports en lecture. 
  
L’indicateur de lecture ne peut pas être modifié pour les éléments suivants :
  
- Messages qui n’existent pas.
    
- Messages déplacés ailleurs.
    
- Messages ouverts avec autorisation de lecture/écriture.
    
- Messages actuellement envoyés.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez décider de ne pas prendre en charge l’envoi de rapports de lecture et la demande de suppression des rapports de lecture. Pour éviter de supprimer un rapport en lecture, retournez MAPI_E_NO_SUPPRESS lorsque **SetReadFlags** est appelé avec SUPPRESS_RECEIPT défini dans le paramètre _ulFlags_ . 
  
Lorsque le paramètre  _lpMsgList_ pointe vers plusieurs messages, effectuez l’opération aussi complètement que possible pour chaque message. N’arrêtez pas l’opération prématurément, à moins qu’une défaillance ne soit hors de votre contrôle, comme un manque de mémoire, un manque d’espace disque ou une altération du magasin de messages. 
  
Si aucun des indicateurs n’est défini dans le paramètre _ulFlags_ , les règles suivantes s’appliquent : 
  
- Si MSGFLAG_READ est déjà défini, ne faites rien.
    
- Si MSGFLAG_READ n’est pas défini, définissez-le immédiatement et envoyez les rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.
    
Lorsque l’indicateur SUPPRESS_RECEIPT est défini, les règles suivantes s’appliquent :
  
- Si MSGFLAG_READ est déjà défini, ne faites rien. 
    
- Si MSGFLAG_READ n’est pas défini, définissez-le et annulez les rapports de lecture en attente.
    
Lorsque l’indicateur CLEAR_READ_FLAG est défini, effacez l’indicateur de MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** de chaque message et n’envoyez aucun rapport de lecture. 
  
Lorsque l’indicateur GENERATE_RECEIPT_ONLY est défini, envoyez tous les rapports en lecture en attente. Ne définissez pas ou n’effacez pas MSGFLAG_READ.
  
Lorsque les indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, définissez **PR_READ_RECEIPT_REQUESTED** sur FALSE s’il est défini et n’envoyez pas de rapport en lecture. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**SetReadFlags** a traité avec succès chaque message. |S_OK  <br/> |
|**SetReadFlags** n’a pas pu traiter correctement chaque message. |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** n’a pas pu se terminer. |Toute valeur d’erreur sauf MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **SetReadFlags** ne peut pas se terminer, ne partez pas du principe qu’aucun travail n’a été effectué. **SetReadFlags** a peut-être pu définir ou effacer l’indicateur MSGFLAG_READ pour un ou plusieurs des messages avant de rencontrer l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::SetReadFlags** pour définir manuellement l’état de lecture sur les messages spécifiés. |
   
## <a name="see-also"></a>Voir aussi

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propriété canonique PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)  
- [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

