---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335762"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un jeton numérique que la méthode [IMAPISession:: ShowForm](imapisession-showform.md) utilise pour accéder à un message. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au message. Le passage de résultats **null** dans l'interface standard, ou [IMessage](imessageimapiprop.md), est utilisé. Le paramètre _lpInterface_ doit être **null** ou IID_IMessage. 
    
 _lpMessage_
  
> dans Pointeur vers le message à afficher dans le formulaire.
    
 _lpulMessageToken_
  
> remarquer Pointeur vers un jeton de message, qui est utilisé par la méthode **IMAPISession:: ShowForm** pour accéder au message pointé par _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La préparation du formulaire a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::P repareform** crée un jeton de message pour le message pointé par le paramètre _lpMessage_ et appelle la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du message. Ce jeton est transmis dans le paramètre _ulMessageToken_ à **IMAPISession:: ShowForm**. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si l'appel à **PrepareForm** réussit, relâchez le message désigné par _lpMessage_ en appelant sa méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) avant d'appeler **ShowForm**. Si vous ne libérez pas le message avant d'appeler **ShowForm** , vous risquez de provoquer des fuites de mémoire. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::P repareform** , ainsi que **IMAPISession:: ShowForm**, pour afficher un message dans un formulaire modal.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

