---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b90460da493fbc9479324c72164ea0600e873f25
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461268"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active le message suivant ou précédent dans l’ordre d’affichage. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Paramètres

_ulDir_
  
> [in] Indicateurs d’état donnant des informations sur le message à activer. Les paramètres d’indicateur valides sont les :
    
  - VCDIR_CATEGORY : la visionneuse doit activer un message dans une autre catégorie de l’affichage. Le message à activer est le suivant : 
        
    - Premier message de la catégorie d’affichage suivante si cet indicateur est **oré** avec VCDIR_NEXT. 
        
    - Dernier message de la catégorie d’affichage précédente si cet indicateur est **ORed** avec VCDIR_PREV et si la catégorie précédente est étendue. 
        
    - Premier message de la catégorie d’affichage précédente si cet indicateur est **ORed** avec VCDIR_PREV et si la catégorie précédente n’est pas étendue. Dans ce cas, la catégorie précédente subit une expansion automatique. 
        
  - VCDIR_DELETE : la visionneuse doit activer le message suivant ou précédent, car le message actif a été supprimé. 
        
  - VCDIR_MOVE : la visionneuse doit activer le message suivant ou précédent, car le message actif a été déplacé. 
        
  - VCDIR_NEXT : la visionneuse doit activer le message suivant dans l’ordre d’affichage. 
        
  - VCDIR_PREV : la visionneuse doit activer le message précédent dans l’ordre d’affichage. 
        
  - VCDIR_UNREAD : la visionneuse doit activer le message non lu suivant ou précédent dans l’ordre d’affichage. 
    
_prcPosRect_
  
> [in] Pointeur vers une Windows **RECT** contenant la taille et la position de la fenêtre à utiliser pour afficher le message activé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été activé avec succès. 
    
S_FALSE 
  
> Le message a été activé avec succès, mais un autre type de formulaire a été ouvert dans le processus.
    
## <a name="remarks"></a>Remarques

Les objets form appellent **la méthode IMAPIViewContext::ActivateNext** pour modifier le message affiché à l’utilisateur. La valeur transmise dans le _paramètre ulDir_ indique quel message doit être activé et, dans certains cas, pourquoi. Les VCDIR_NEXT et VCDIR_PREVIOUS d’affichage correspondent aux utilisateurs qui choisissent respectivement la commande  Suivante ou  Précédente dans un affichage. Ces opérations correspondent généralement à un déplacement vers le haut ou vers le bas d’un message dans la liste des messages de la visionneuse de formulaires. 
  
Les indicateurs VCDIR_DELETE et VCDIR_MOVE sont définies par les méthodes [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) et [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) , respectivement. Les implémentations de ces méthodes appellent **ActivateNext** avec le sens approprié, puis effectuent l’opération demandée sur le message si l’appel **ActivateNext** n’a pas échoué. Les visionneuses de formulaires permettent généralement aux utilisateurs de spécifier le sens de déplacement dans la liste des messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Votre implémentation de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) effectue le message suivant ou précédent dans le dossier, en fonction de la valeur de  _ulDir_, le message actuel. Après **le retour d’ActivateNext** , appelez [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) pour obtenir un pointeur vers le message nouvellement activé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si **ActivateNext** renvoie S_FALSE, ou si un message actuel n’est pas présent, effectuez votre procédure d’arrêt normal qui doit inclure l’appel de la méthode [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) de votre formulaire. Si un message suivant ou précédent s’affiche, utilisez le rectangle de fenêtre transmis dans le paramètre _prcPosRect_ pour l’afficher. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implémente la **méthode IMAPIViewContext::ActivateNext** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

