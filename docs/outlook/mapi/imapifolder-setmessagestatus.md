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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342776"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l'état associé à un message (par exemple, si ce message est marqué pour suppression).
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée pour le message dont l'État est défini.
    
 _ulNewStatus_
  
> dans Nouvel État à affecter. 
    
 _ulNewStatusMask_
  
> dans Masque de des indicateurs qui est appliqué au nouvel État et indique les indicateurs à définir. Les indicateurs suivants peuvent être définis:
    
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
    
 _lpulOldStatus_
  
> remarquer Pointeur vers l'état précédent du message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'état du message a été correctement défini.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: SetMessageStatus** définit l'état du message sur la valeur stockée dans sa propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La manière dont les bits d'état des messages sont définis, effacés et utilisés dépend entièrement de votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être nuls. 
  
L'implémentation d'un fournisseur de transport distant de cette méthode doit respecter les sémantiques décrites ici. Il n'y a aucune considération particulière. Les clients utilisent cette méthode pour définir les bits MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE pour indiquer qu'un message particulier doit être téléchargé ou supprimé de la Banque de messages distante. Un fournisseur de transport distant n'a pas besoin d'implémenter la méthode [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) associée. Les clients doivent consulter la table des matières du dossier pour déterminer l'état d'un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la propriété **PR_MSG_STATUS** d'un message pour négocier une opération de verrouillage de message avec d'autres clients. DéSignez un bit comme bit de verrouillage. Pour déterminer si le bit de verrouillage a été défini, examinez la valeur précédente de l'état du message dans le paramètre _lpulOldStatus_ . Utilisez les autres bits dans le paramètre _ulNewStatus_ pour suivre l'état du message sans interférer avec le bit de verrouillage. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

