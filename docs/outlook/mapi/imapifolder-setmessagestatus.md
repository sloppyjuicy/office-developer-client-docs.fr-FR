---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d06523625a20760faec7a6c73a6beaef757818b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575076"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l’état associé à un message (par exemple, si ce message est marqué pour suppression).
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message dont le statut est défini.
    
 _ulNewStatus_
  
> [in] Le nouveau statut à affecter. 
    
 _ulNewStatusMask_
  
> [in] Masque de bits d’indicateurs qui est appliqué à l’état de nouveau et indique les indicateurs à définir. Les indicateurs suivants peuvent être définis :
    
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
    
 _lpulOldStatus_
  
> [out] Pointeur vers l’état précédent du message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le statut du message a été correctement défini.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::SetMessageStatus** définit l’état de message à la valeur qui est stockée dans sa propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Comment les bits d’état message définis, désactivées et utilisés dépendent complètement votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être égal à zéro. 
  
Implémentation d’un fournisseur de transport à distance de cette méthode doit suivre la sémantique décrite ici. Il n’existe pas de considérations particulières. Les clients utilisent cette méthode pour définir les bits MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE pour indiquer qu’un message particulier doivent être téléchargées ou supprimé de la banque de messages à distance. Un fournisseur de transport à distance ne dispose pas d’implémenter la méthode [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) associée. Clients doivent rechercher dans le tableau de contenu du dossier pour déterminer l’état d’un message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser la propriété **PR_MSG_STATUS** d’un message de négocier une opération de verrouillage du message avec d’autres clients. Désigner un peu comme le bit de verrouillage. Pour déterminer si le bit de verrouillage a été défini, examinez la valeur précédente pour le statut du message dans le paramètre _lpulOldStatus_ . Utilisez les autres fichiers binaires dans le paramètre _ulNewStatus_ pour effectuer le suivi du statut du message sans interférer avec le bit de verrouillage. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

