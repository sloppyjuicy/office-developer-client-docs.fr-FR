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
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783736"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**S’applique à**: Outlook 
  
Obtient l’état associé à un message dans un dossier spécifique (par exemple, si ce message est marqué pour suppression).
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message dont l’état est obtenu.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulMessageStatus_
  
> [out] Pointeur vers un pointeur vers un masque de bits d’indicateurs qui indiquent l’état du message. Bits 0 à 15 sont réservés et doivent être égal à zéro ; bits 16 à 31 sont disponibles pour une utilisation spécifique à l’implémentation. Les indicateurs suivants peuvent être définis :
    
MSGSTATUS_DELMARKED 
  
> Le message a été marqué pour suppression.
    
MSGSTATUS_HIDDEN 
  
> Le message ne pas doit être affichée. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Le message doit être affichée en surbrillance.
    
MSGSTATUS_REMOTE_DELETE 
  
> Le message a été marqué pour suppression au niveau de la banque de messages à distance sans télécharger sur le client local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Le message a été marqué pour téléchargement à partir de la banque de messages à distance au client local.
    
MSGSTATUS_TAGGED 
  
> Le message a été marqué pour un usage défini par le client.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le statut du message a été récupéré correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::GetMessageStatus** renvoie l’état d’un message. Statut du message est stocké dans la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Comment les bits d’état message définis, désactivées et utilisés dépendent complètement votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être égal à zéro. Si vous stockez les messages dans la sous-arborescence IPM, MAPI réserve bits 16 à 31 pour une utilisation par les clients IPM. Si vous stockez les messages dans d’autres sous-arborescences, vous pouvez utiliser les bits 16 à 31 selon vos besoins.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message suivant s’affiche.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal et OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message à afficher à transmettre à la visionneuse de formulaire, qui est CMyMAPIFormViewer ou [IMAPISession::ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

