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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d4b62c4131ecc58db6957144321146625b43f7bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591022"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée un jeton numérique que la méthode [IMAPISession::ShowForm](imapisession-showform.md) utilise pour accéder à un message. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message. Transmission des résultats **null** dans l’interface standard ou [IMessage](imessageimapiprop.md), utilisés. Le paramètre _lpInterface_ doit être **null** ou IID_IMessage. 
    
 _lpMessage_
  
> [in] Pointeur vers le message à afficher dans le formulaire.
    
 _lpulMessageToken_
  
> [out] Pointeur vers un jeton de message, qui est utilisé par la méthode **IMAPISession::ShowForm** pour accéder au message vers lequel pointé _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le formulaire a été correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::PrepareForm** crée un jeton de message pour le message vers laquelle pointé le paramètre _lpMessage_ et appelle la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) du message. Ce jeton est transmis dans le paramètre _ulMessageToken_ à **IMAPISession::ShowForm**. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si l’appel **PrepareForm** réussit, libérer le message vers lequel pointé _lpMessage_ en appelant la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) avant d’appeler **ShowForm**. Pour libérer le message avant d’appeler **ShowForm** peut provoquer des fuites de mémoire. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::PrepareForm** , ainsi **IMAPISession::ShowForm**, pour afficher un message dans un formulaire modal.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

