---
title: IMAPIMessageSiteSubmitMessage
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fce66a5c7a306df2d116f473458e7155739eb750
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630697"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le message actuel soit mis en file d’attente pour remise.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont un message est envoyé. L’indicateur suivant peut être définie :
    
FORCE_SUBMIT 
  
> MAPI doit envoyer le message même s’il est possible qu’il ne soit pas envoyé immédiatement.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIMessageSite::SubmitMessage** pour demander qu’un message soit mis en file d’attente pour remise. Le site de message doit appeler la [méthode IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) avant d’envoyer le message. Le message n’a pas besoin d’être enregistré précédemment, car **SubmitMessage** doit provoquer l’enregistrée si le message a été modifié. Après le retour de **SubmitMessage,** le formulaire doit vérifier la recherche d’un message en cours, puis se fermer s’il n’en existe aucun. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI utilise la **méthode IMAPIMessageSite::SubmitMessage** pour enregistrer le message. Tout d’abord, il appelle la méthode **IPersistMessage::HandsOffMessage,** puis **submitMessage**.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

