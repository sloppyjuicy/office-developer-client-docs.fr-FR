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
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783741"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**S’applique à**: Outlook 
  
Définit ou supprime l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs des messages du dossier et gère l’envoi de rapports de lecture. 
  
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
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient l’ou les messages que vous ont lu les indicateurs pour définir ou supprimer. Si _lpMsgList_ est défini sur NULL, la lecture indicateurs pour tous les messages du dossier sont configurés ou désactivés. 
    
_ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
_lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de mise en œuvre de MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
_ulFlags_
  
> [in] Un masque de bits d’indicateurs qui contrôlent la valeur d’indicateur de lecture d’un message et le traitement de lire des rapports. Les indicateurs suivants peuvent être définis :
    
  - CLEAR_READ_FLAG : L’indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé. 
        
  - CLEAR_NRN_PENDING : L’indicateur MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport non lu ne doit pas être envoyé. 
        
  - CLEAR_RN_PENDING : L’indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé. 
        
  - GENERATE_RECEIPT_ONLY : Un rapport de lecture doit être envoyé si un est en attente, mais il ne doit y avoir aucune modification de l’état de l’indicateur MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS : Permet de **SetReadFlags** renvoyer avec succès, éventuellement, avant la fin de l’opération. 
        
  - MESSAGE_DIALOG : Affiche un indicateur de progression pendant que l’opération s’effectue.
    
  - SUPPRESS_RECEIPT : Un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et cet appel remplace l’état du message non lu à lire. Si cet appel ne modifie pas l’état du message, le fournisseur de banque de message peut ignorer cet indicateur.
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
> L’indicateur de lecture pour l’ou les messages spécifié a été correctement configurée ou désactivée.
    
MAPI_E_NO_SUPPRESS 
  
> Le fournisseur de banque de messages ne gère pas la suppression des rapports de lecture.
    
MAPI_E_INVALID_PARAMETER 
  
> Une des combinaisons d’indicateurs incompatibles suivants est définie dans le paramètre _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais pas tous les messages ont été traités. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::SetReadFlags** Active ou désactive l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** d’une ou plusieurs des messages du dossier. Définition de l’indicateur MSGFLAG_READ marque un message comme lu, ce qui n’indique pas nécessairement que le destinataire a lu réellement le message. 
  
**SetReadFlags** gère également l’envoi des rapports de lecture. 
  
L’indicateur de lecture ne peut pas être modifié pour les éléments suivants :
  
- Messages qui n’existent pas.
    
- Les messages qui ont été déplacés vers un autre emplacement.
    
- Messages qui sont ouvertes avec l’autorisation de lecture/écriture.
    
- Messages qui sont actuellement envoyées.
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous décider de ne pas prendre en charge l’envoi de rapports de lecture et de la demande à supprimer les rapports de lecture. Pour éviter la suppression d’un rapport de lecture, renvoyer MAPI_E_NO_SUPPRESS lorsque **SetReadFlags** est appelée avec SUPPRESS_RECEIPT dans le paramètre _ulFlags_ . 
  
Lorsque le paramètre _lpMsgList_ pointe vers plus d’un message, effectuez l’opération complètement que possible pour chaque message. N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages. 
  
Si aucun des indicateurs sont définies dans le paramètre _ulFlags_ , les règles suivantes s’appliquent : 
  
- Si MSGFLAG_READ est déjà défini, ne faites rien.
    
- Si MSGFLAG_READ n’est pas défini, affectez-lui immédiatement et envoyer tout en attente de rapports de lecture si la valeur de la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Lorsque l’indicateur SUPPRESS_RECEIPT est défini, les règles suivantes s’appliquent :
  
- Si MSGFLAG_READ est déjà défini, ne faites rien. 
    
- Si MSGFLAG_READ n’est pas définie, définissez-la et annuler les en attente de rapports de lecture.
    
Lorsque l’indicateur CLEAR_READ_FLAG est défini, effacer l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** du chaque message et ne pas envoyer des rapports de lecture. 
  
Lorsque l’indicateur GENERATE_RECEIPT_ONLY est défini, envoyer des rapports de lecture en attente. Ne pas définir ou effacer MSGFLAG_READ.
  
Lorsque les indicateurs GENERATE_RECEIPT_ONLY et SUPPRESS_RECEIPT sont définies, la valeur **PR_READ_RECEIPT_REQUESTED** FALSE si elle est définie et ne pas envoyer un rapport de lecture. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Prévoyez ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**SetReadFlags** a traité avec succès à chaque message.  <br/> |S_OK  <br/> |
|**SetReadFlags** n’a pas pu traiter correctement tous les messages.  <br/> |MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** n’a pas pu terminer.  <br/> |Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **SetReadFlags** est impossible de terminer, ne supposent qu’aucun travail n’a été effectuée. **SetReadFlags** a pu définir ou effacer l’indicateur MSGFLAG_READ pour une ou plusieurs des messages avant de rencontrer l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
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
- [Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)

