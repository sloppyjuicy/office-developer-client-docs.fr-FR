---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321405"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le message en cours soit mis en file d'attente pour remise.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'envoi d'un message. L'indicateur suivant peut être défini:
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message même s'il ne peut pas être envoyé immédiatement.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIMessageSite:: SubmitMessage** pour demander qu'un message soit mis en file d'attente pour remise. Le site de message doit appeler la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) avant d'envoyer le message. Le message n'a pas besoin d'avoir été précédemment enregistré, car **SubmitMessage** doit entraîner l'enregistrement du message si celui-ci a été modifié. Après le retour de **SubmitMessage**, le formulaire doit vérifier l'existence d'un message en cours, puis le faire disparaître s'il n'en existe pas. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SubmitMessage  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite:: SubmitMessage** pour enregistrer le message. Tout d'abord, il appelle la méthode **IPersistMessage:: HandsOffMessage** , puis appelle **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

