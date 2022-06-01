---
title: IMAPIMessageSiteSubmitMessage
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIMessageSiteSubmitMessage, qui demande que le message actuel soit mis en file d’attente pour la remise.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
ms.openlocfilehash: 9e496eb9bc93664484665a607350d939e5784275
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812109"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le message actuel soit mis en file d’attente pour la remise.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont un message est envoyé. L’indicateur suivant peut être défini :
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message même s’il peut ne pas être envoyé immédiatement.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIMessageSite::SubmitMessage** pour demander qu’un message soit mis en file d’attente pour la remise. Le site de message doit appeler la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) avant d’envoyer le message. Le message n’a pas besoin d’être enregistré précédemment, car **SubmitMessage** doit entraîner l’enregistrement du message si le message a été modifié. Après le retour de **SubmitMessage**, le formulaire doit rechercher un message actif, puis se faire ignorer s’il n’en existe aucun. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, consultez [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::SubmitMessage** pour enregistrer le message. Tout d’abord, il appelle la méthode **IPersistMessage::HandsOffMessage** , puis **il appelle SubmitMessage**. |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

