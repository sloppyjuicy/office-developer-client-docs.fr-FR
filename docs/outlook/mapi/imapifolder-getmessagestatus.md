---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350952"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient l'état associé à un message dans un dossier spécifique (par exemple, si ce message est marqué pour suppression).
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée pour le message dont l'État est obtenu.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulMessageStatus_
  
> remarquer Pointeur vers un pointeur vers un masque de réindicateur qui indique l'état du message. Les bits 0 à 15 sont réservés et doivent être nuls; les bits 16 à 31 sont disponibles pour une utilisation propre à l'implémentation. Les indicateurs suivants peuvent être définis:
    
MSGSTATUS_DELMARKED 
  
> Le message a été marqué pour suppression.
    
MSGSTATUS_HIDDEN 
  
> Le message ne doit pas être affiché. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Le message doit être affiché en surbrillance.
    
MSGSTATUS_REMOTE_DELETE 
  
> Le message a été marqué pour suppression dans le magasin de messages distant sans téléchargement vers le client local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Le message a été marqué pour téléchargement depuis le magasin de messages distant vers le client local.
    
MSGSTATUS_TAGGED 
  
> Le message a été marqué pour un objectif défini par le client.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'état du message a été correctement récupéré.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: GetMessageStatus** renvoie l'état d'un message. L'état du message est stocké dans la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La manière dont les bits d'état des messages sont définis, effacés et utilisés dépend entièrement de votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être nuls. Si vous stockez des messages dans la sous-arborescence IPM, MAPI réserve les bits 16 à 31 aux clients IPM. Si vous stockez des messages dans d'autres sous-arborescences, vous pouvez utiliser les bits 16 à 31 à vos fins.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetNextMessage  <br/> |MFCMAPI utilise la méthode **IMAPIFolder:: GetMessageStatus** pour obtenir l'état du prochain message à afficher.  <br/> |
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal et OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPIFolder:: GetMessageStatus** pour obtenir l'état du message à afficher pour transmettre à la visionneuse de formulaires, qui est CMyMAPIFormViewer ou [IMAPISession:: ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

