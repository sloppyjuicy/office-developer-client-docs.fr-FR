---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406912"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou désine l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier et gère l’envoi de rapports de lecture. 
  
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
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages qui ont des indicateurs de lecture à définir ou effacer. Si  _lpMsgList_ est définie sur NULL, les indicateurs de lecture de tous les messages du dossier sont définies ou effacées. 
    
_ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression. Le _paramètre ulUIParam_ est ignoré, sauf si l’MESSAGE_DIALOG est définie dans _le paramètre ulFlags._ 
    
_lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans  _ulFlags_.
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la définition de l’indicateur de lecture d’un message et le traitement des rapports de lecture. Les indicateurs suivants peuvent être définies :
    
  - CLEAR_READ_FLAG : l’indicateur MSGFLAG_READ doit être  effacé dans PR_MESSAGE_FLAGS et un rapport de lecture ne doit pas être envoyé. 
        
  - CLEAR_NRN_PENDING : l’indicateur MSGFLAG_NRN_PENDING doit être effacé  dans PR_MESSAGE_FLAGS et un rapport non lu ne doit pas être envoyé. 
        
  - CLEAR_RN_PENDING : l’indicateur MSGFLAG_RN_PENDING doit être  effacé dans PR_MESSAGE_FLAGS et un rapport de lecture ne doit pas être envoyé. 
        
  - GENERATE_RECEIPT_ONLY : un rapport de lecture doit être envoyé s’il est en attente, mais l’état de l’indicateur MSGFLAG_READ ne doit pas être changé.
        
  - MAPI_DEFERRED_ERRORS : permet à **SetReadFlags** de renvoyer correctement, éventuellement avant la fin de l’opération. 
        
  - MESSAGE_DIALOG : affiche un indicateur de progression pendant la progression de l’opération.
    
  - SUPPRESS_RECEIPT : un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel modifie l’état du message de non lu en lecture. Si cet appel ne modifie pas l’état du message, le fournisseur de la boutique de messages peut ignorer cet indicateur.
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
> L’indicateur de lecture du ou des messages spécifiés a été correctement définie ou effacée.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur de la boutique de messages ne prend pas en charge la suppression des rapports de lecture.
    
MAPI_E_INVALID_PARAMETER 
  
> L’une des combinaisons d’indicateurs incompatibles suivantes est définie dans le  _paramètre ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais tous les messages n’ont pas été correctement traitées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::SetReadFlags** définit ou désinsiste l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** d’un ou plusieurs messages du dossier. La définition MSGFLAG_READ marque un message comme lu, ce qui n’indique pas nécessairement que le destinataire prévu a réellement lu le message. 
  
**SetReadFlags gère** également l’envoi de rapports de lecture. 
  
L’indicateur de lecture ne peut pas être modifié pour les raisons suivantes :
  
- Messages qui n’existent pas.
    
- Messages qui ont été déplacés ailleurs.
    
- Messages ouverts avec une autorisation de lecture/écriture.
    
- Messages actuellement envoyés.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez décider de ne pas prendre en charge l’envoi de rapports de lecture et la demande de suppression des rapports de lecture. Pour éviter la suppression d’un rapport de lecture, renvoyez MAPI_E_NO_SUPPRESS lorsque **SetReadFlags** est appelé avec SUPPRESS_RECEIPT définie dans le _paramètre ulFlags._ 
  
Lorsque le  _paramètre lpMsgList_ pointe vers plusieurs messages, effectuez l’opération aussi complètement que possible pour chaque message. N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages. 
  
Si aucun des indicateurs n’est paramétré dans  _le paramètre ulFlags,_ les règles suivantes s’appliquent : 
  
- Si MSGFLAG_READ est déjà définie, ne faites rien.
    
- Si MSGFLAG_READ n’est pas définie, définissez-la immédiatement et envoyez les rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.
    
Lorsque l’SUPPRESS_RECEIPT est définie, les règles suivantes s’appliquent :
  
- Si MSGFLAG_READ est déjà définie, ne faites rien. 
    
- Si MSGFLAG_READ n’est pas définie, définissez-la et annulez les rapports de lecture en attente.
    
Lorsque l’CLEAR_READ_FLAG est définie, effacer l’indicateur MSGFLAG_READ dans la  propriété PR_MESSAGE_FLAGS de chaque message et n’envoyez aucun rapport de lecture. 
  
Lorsque l’GENERATE_RECEIPT_ONLY est définie, envoyez les rapports de lecture en attente. Ne pas définir ou effacer les MSGFLAG_READ.
  
Lorsque les indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont tous deux définies, définissez PR_READ_RECEIPT_REQUESTED sur FALSE **si** elle est définie et n’envoyez pas de rapport de lecture. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**SetReadFlags a** correctement traitée chaque message.  <br/> |S_OK  <br/> |
|**SetReadFlags n’a** pas pu traiter correctement chaque message.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags n’a** pas pu se terminer.  <br/> |Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **SetReadFlags ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué. **SetReadFlags** a peut-être pu définir ou effacer l’indicateur MSGFLAG_READ’un ou plusieurs des messages avant de rencontrer l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::SetReadFlags** pour définir manuellement l’état de lecture sur les messages spécifiés.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propriété canonique PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)  
- [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

