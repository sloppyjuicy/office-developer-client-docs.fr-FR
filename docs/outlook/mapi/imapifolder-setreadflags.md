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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350987"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou efface l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d'un ou plusieurs des messages du dossier, et gère l'envoi des rapports de lecture. 
  
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
  
> dans Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages dont les indicateurs de lecture doivent être définis ou désactivés. Si _lpMsgList_ est défini sur null, les indicateurs de lecture de tous les messages du dossier sont définis ou effacés. 
    
_ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
_lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
_ulFlags_
  
> dans Masque de réinitialisation des indicateurs qui contrôle le paramétrage de l'indicateur de lecture d'un message et le traitement des rapports de lecture. Les indicateurs suivants peuvent être définis:
    
  - CLEAR_READ_FLAG: l'indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé. 
        
  - CLEAR_NRN_PENDING: l'indicateur MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport non lu ne doit pas être envoyé. 
        
  - CLEAR_RN_PENDING: l'indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé. 
        
  - GENERATE_RECEIPT_ONLY: un rapport de lecture doit être envoyé s'il en est en attente, mais il ne doit y avoir aucune modification dans l'état de l'indicateur MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS: permet à **SetReadFlags** de renvoyer correctement, éventuellement avant la fin de l'opération. 
        
  - MESSAGE_DIALOG: affiche un indicateur de progression pendant l'exécution de l'opération.
    
  - SUPPRESS_RECEIPT: un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel change l'état du message de non lu en lecture. Si cet appel ne modifie pas l'état du message, le fournisseur de banque de messages peut ignorer cet indicateur.
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
> L'indicateur de lecture pour le ou les messages spécifiés a été correctement défini ou désactivé.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur de banque de messages ne prend pas en charge la suppression des rapports lus.
    
MAPI_E_INVALID_PARAMETER 
  
> L'une des combinaisons d'indicateurs incompatibles suivantes est définie dans le paramètre _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'appel a réussi, mais tous les messages n'ont pas été traités avec succès. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: SetReadFlags** définit ou efface l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** d'un ou plusieurs messages du dossier. La définition de l'indicateur MSGFLAG_READ marque un message comme lu, ce qui ne signifie pas nécessairement que le destinataire concerné a effectivement lu le message. 
  
**SetReadFlags** gère également l'envoi des rapports de lecture. 
  
L'indicateur de lecture ne peut pas être modifié pour les éléments suivants:
  
- Messages qui n'existent pas.
    
- Messages qui ont été déplacés ailleurs.
    
- Messages ouverts avec une autorisation en lecture/écriture.
    
- Messages actuellement envoyés.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez décider de ne pas prendre en charge l'envoi de rapports de lecture et la demande de suppression des rapports de lecture. Pour éviter la suppression d'un rapport de lecture, renvoyez MAPI_E_NO_SUPPRESS lorsque **SetReadFlags** est appelé avec SUPPRESS_RECEIPT défini dans le paramètre _ulFlags_ . 
  
Lorsque le paramètre _lpMsgList_ pointe vers plusieurs messages, effectuez l'opération aussi complètement que possible pour chaque message. N'arrêtez pas l'opération prématurément à moins qu'une défaillance ne se produise au-delà de votre contrôle, telle qu'une mémoire insuffisante, un manque d'espace disque ou une corruption de la Banque de messages. 
  
Si aucun des indicateurs n'est défini dans le paramètre _ulFlags_ , les règles suivantes s'appliquent: 
  
- Si MSGFLAG_READ est déjà défini, ne faites rien.
    
- Si MSGFLAG_READ n'est pas défini, définissez-le immédiatement et envoyez tous les rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.
    
Lorsque l'indicateur SUPPRESS_RECEIPT est défini, les règles suivantes s'appliquent:
  
- Si MSGFLAG_READ est déjà défini, ne faites rien. 
    
- Si MSGFLAG_READ n'est pas défini, définissez-le et annulez tous les rapports de lecture en attente.
    
Lorsque l'indicateur CLEAR_READ_FLAG est défini, effacez l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** de chaque message et n'envoyez aucun rapport de lecture. 
  
Lorsque l'indicateur GENERATE_RECEIPT_ONLY est défini, envoyez tous les rapports de lecture en attente. Ne définissez pas MSGFLAG_READ.
  
Lorsque les deux indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, définissez **PR_READ_RECEIPT_REQUESTED** sur false s'il est défini et ne pas envoyer de rapport de lecture. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoyée**|
|:-----|:-----|
|**SetReadFlags** a réussi à traiter tous les messages.  <br/> |S_OK  <br/> |
|**SetReadFlags** n'a pas pu traiter correctement tous les messages.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** n'a pas pu être exécuté.  <br/> |Toute valeur d'erreur à l'exception de MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **SetReadFlags** ne parvient pas à terminer, ne partez pas du principe qu'aucun travail n'a été effectué. **SetReadFlags** peut avoir pu définir ou effacer l'indicateur MSGFLAG_READ pour un ou plusieurs messages avant de rencontrer l'erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI utilise la méthode **IMAPIFolder:: SetReadFlags** pour définir manuellement l'état de lecture des messages spécifiés.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propriété canonique PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)  
- [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

