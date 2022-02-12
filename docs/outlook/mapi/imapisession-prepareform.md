---
title: IMAPISessionPrepareForm
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 04a3ba5b1af8b3a2c37864410d5f280a7d030f0c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770758"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message. La **transmission de** null entraîne l’utilisation de l’interface standard, [ou IMessage](imessageimapiprop.md). Le  _paramètre lpInterface_ doit être **null** ou IID_IMessage. 
    
 _lpMessage_
  
> [in] Pointeur vers le message à afficher dans le formulaire.
    
 _lpulMessageToken_
  
> [out] Pointeur vers un jeton de message, utilisé par la méthode **IMAPISession::ShowForm** pour accéder au message pointé par  _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La préparation du formulaire a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::P repareForm** crée un jeton de message pour le message pointé par le paramètre  _lpMessage_ et appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du message. Ce jeton est transmis dans le _paramètre ulMessageToken_ à **IMAPISession::ShowForm**. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si l’appel à **PrepareForm** réussit, relâchez le message pointé par  _lpMessage_ en appelant sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) avant d’appeler **ShowForm**. L’échec de la libération du message avant l’appel **de ShowForm** peut provoquer des fuites de mémoire. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::P repareForm** , avec **IMAPISession::ShowForm**, pour afficher un message sous forme modale. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

