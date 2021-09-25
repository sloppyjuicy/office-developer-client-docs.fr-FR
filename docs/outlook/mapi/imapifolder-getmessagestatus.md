---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 762935b5e569dd63399862f32945599c0dc5df09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571806"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient l’état associé à un message dans un dossier particulier (par exemple, si ce message est marqué pour suppression).
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message dont l’état est obtenu.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulMessageStatus_
  
> [out] Pointeur vers un pointeur vers un masque de bits d’indicateurs qui indiquent l’état du message. Les bits 0 à 15 sont réservés et doivent être zéro ; Les bits 16 à 31 sont disponibles pour une utilisation spécifique à l’implémentation. Les indicateurs suivants peuvent être définies :
    
MSGSTATUS_DELMARKED 
  
> Le message a été marqué pour suppression.
    
MSGSTATUS_HIDDEN 
  
> Le message ne doit pas être affiché. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Le message doit être affiché en surbrillant.
    
MSGSTATUS_REMOTE_DELETE 
  
> Le message a été marqué pour suppression dans la boutique de messages distante sans téléchargement vers le client local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Le message a été marqué pour téléchargement à partir de la boutique de messages distante vers le client local.
    
MSGSTATUS_TAGGED 
  
> Le message a été marqué à des fins définies par le client.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état du message a été récupéré avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::GetMessageStatus** renvoie l’état d’un message. L’état du message est stocké dans la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La façon dont les bits d’état du message sont définies, effacées et utilisées dépend entièrement de votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être zéro. Si vous stockez des messages dans la sous-arbre IPM, MAPI réserve les bits 16 à 31 pour une utilisation par les clients IPM. Si vous stockez des messages dans d’autres sous-arbre, vous pouvez utiliser les bits 16 à 31 à vos propres fins.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message suivant à afficher.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal et OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message à afficher pour passer à la visionneuse de formulaires, c’est-à-dire CMyMAPIFormViewer ou [IMAPISession::ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

