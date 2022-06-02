---
title: IMAPISessionPrepareForm
description: IMAPISessionPrepareForm crée un jeton numérique que la méthode IMAPISessionShowForm utilise pour accéder à un message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
ms.openlocfilehash: 6914ac92cb68cfec0ce931cd800fcc4504880291
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827939"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un jeton numérique utilisé par la méthode [IMAPISession::ShowForm](imapisession-showform.md) pour accéder à un message. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message. Le passage de **la valeur Null** entraîne l’utilisation de l’interface standard, ou [IMessage](imessageimapiprop.md). Le paramètre  _lpInterface_ doit être **null** ou IID_IMessage. 
    
 _lpMessage_
  
> [in] Pointeur vers le message à afficher dans le formulaire.
    
 _lpulMessageToken_
  
> [out] Pointeur vers un jeton de message, qui est utilisé par la méthode **IMAPISession::ShowForm** pour accéder au message pointé par  _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La préparation du formulaire a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::P repareForm** crée un jeton de message pour le message pointé par le paramètre  _lpMessage_ et appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du message. Ce jeton est passé dans le paramètre _ulMessageToken_ à **IMAPISession::ShowForm**. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si l’appel à **PrepareForm** réussit, relâchez le message pointé par  _lpMessage_ en appelant sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) avant d’appeler **ShowForm**. Le fait de ne pas libérer le message avant d’appeler **ShowForm** peut provoquer des fuites de mémoire. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::P repareForm** , ainsi **que IMAPISession::ShowForm**, pour afficher un message dans un formulaire modal. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

