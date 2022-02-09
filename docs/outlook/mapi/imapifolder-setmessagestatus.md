---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1896e413a1a98973260a239d6aea1cb49bb7068b
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462458"
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message dont l’état est définie.
    
 _ulNewStatus_
  
> [in] Nouveau statut à attribuer. 
    
 _ulNewStatusMask_
  
> [in] Masque de bits d’indicateurs appliqué au nouvel état et qui indique les indicateurs à définir. Les indicateurs suivants peuvent être définies :
    
MSGSTATUS_DELMARKED 
  
> Le message a été marqué pour suppression.
    
MSGSTATUS_HIDDEN 
  
> Le message ne doit pas être affiché.
    
MSGSTATUS_HIGHLIGHTED 
  
> Le message doit être affiché en surbrillant.
    
MSGSTATUS_REMOTE_DELETE 
  
> Le message a été marqué pour suppression dans la boutique de messages distante sans téléchargement sur le client local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Le message a été marqué pour téléchargement à partir de la boutique de messages distante vers le client local.
    
MSGSTATUS_TAGGED 
  
> Le message a été marqué à des fins définies par le client.
    
 _lpulOldStatus_
  
> [out] Pointeur vers l’état précédent du message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état du message a été correctement définie.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::SetMessageStatus** définit l’état du message sur la valeur stockée dans sa propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La façon dont les bits d’état de message sont définies, effacées et utilisées dépend entièrement de votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être zéro. 
  
L’implémentation de cette méthode par un fournisseur de transport distant doit suivre la sémantique décrite ici. Il n’existe aucune considération particulière. Les clients utilisent cette méthode pour définir les bits MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE pour indiquer qu’un message particulier doit être téléchargé ou supprimé de la boutique de messages distante. Un fournisseur de transport distant n’a pas besoin d’implémenter la méthode [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) associée. Les clients doivent rechercher dans la table des matières du dossier pour déterminer l’état d’un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la **propriété PR_MSG_STATUS** d’un message pour négocier une opération de verrouillage de message avec d’autres clients. Désignez un bit comme bit de verrouillage. Pour déterminer si le bit de verrouillage a été définie, examinez la valeur précédente pour l’état du message dans _le paramètre lpulOldStatus_ . Utilisez les autres bits du paramètre _ulNewStatus_ pour suivre l’état du message sans interférer avec le bit de verrouillage. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

