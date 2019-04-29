---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405897"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une pièce jointe. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Paramètres

 _ulAttachmentNum_
  
> dans Numéro d'index de la pièce jointe à ouvrir, tel qu'il est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe. Ce numéro d'index identifie de manière unique la pièce jointe dans le message et est valide uniquement dans le contexte du message.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) représentant l'interface à utiliser pour accéder à la pièce jointe. Le fait de transmettre des résultats NULL dans l'interface standard de la pièce jointe, ou **IAttach**, est renvoyé. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont la pièce jointe est ouverte. Les indicateurs suivants peuvent être définis: 
    
MAPI_BEST_ACCESS 
  
> Demande l'ouverture de la pièce jointe avec les autorisations réseau maximales accordées à l'utilisateur et l'accès maximal de l'application cliente. Par exemple, si le client dispose d'une autorisation en lecture/écriture, la pièce jointe doit être ouverte avec une autorisation en lecture/écriture; Si le client dispose d'un accès en lecture seule, la pièce jointe doit être ouverte avec un accès en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenAttach** de renvoyer correctement, éventuellement avant que la pièce jointe soit entièrement disponible pour le client appelant. Si la pièce jointe n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les pièces jointes sont ouvertes avec un accès en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
 _lppAttach_
  
> remarquer Pointeur vers un pointeur vers la pièce jointe ouverte.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La pièce jointe a été ouverte.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage:: OpenAttach** ouvre la pièce jointe d'un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour ouvrir une pièce jointe, vous devez avoir accès à son numéro de pièce jointe ou à sa propriété **PR_ATTACH_NUM** . Appelez [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) pour récupérer la table de pièces jointes du message et recherchez la ligne qui représente la pièce jointe à ouvrir. Pour plus d'informations, consultez la rubrique [ouverture d'une pièce jointe](opening-an-attachment.md) . 
  
N'essayez pas d'ouvrir une pièce jointe plusieurs fois; les résultats ne sont pas définis et dépendants du fournisseur de banque de messages.
  
Vous pouvez demander que la pièce jointe soit ouverte en mode lecture/écriture, au lieu du mode de lecture seule par défaut. Toutefois, si la pièce jointe est ouverte en mode lecture/écriture, c'est au fournisseur de banque de messages de s'ouvrir. Vous pouvez essayer de modifier la pièce jointe, de préparer la gestion d'un échec possible ou de vérifier le niveau d'accès accordé en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de la pièce jointe, si elle est disponible. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp utilisé pour  <br/> |CAttachmentsDlg:: OpenItemProp  <br/> |MFCMAPI utilise la méthode **IMessage:: OpenAttach** pour ouvrir les objets Attachment,  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

