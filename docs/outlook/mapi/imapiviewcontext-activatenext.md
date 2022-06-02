---
title: IMAPIViewContextActivateNext
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIViewContext ActivateNext, qui active le message suivant ou précédent dans l’ordre d’affichage.
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
ms.openlocfilehash: 921abe8edbf73f073210128ef6c24de93843d97a
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827778"
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
  
> [in] Indicateurs d’état qui donnent des informations sur le message à activer. Les paramètres d’indicateur valides sont les suivants :
    
  - VCDIR_CATEGORY : la visionneuse doit activer un message dans une autre catégorie de la vue. Le message à activer est le suivant : 
        
    - Premier message dans la catégorie d’affichage suivante si cet indicateur est **OR** associé à VCDIR_NEXT. 
        
    - Dernier message de la catégorie d’affichage précédente si cet indicateur est **OR** associé à VCDIR_PREV et si la catégorie précédente est développée. 
        
    - Premier message de la catégorie d’affichage précédente si cet indicateur est **OR** associé à VCDIR_PREV et si la catégorie précédente n’est pas développée. Dans ce cas, la catégorie précédente subit une expansion automatique. 
        
  - VCDIR_DELETE : la visionneuse doit activer le message suivant ou précédent, car le message actuel a été supprimé. 
        
  - VCDIR_MOVE : la visionneuse doit activer le message suivant ou précédent, car le message actuel a été déplacé. 
        
  - VCDIR_NEXT : la visionneuse doit activer le message suivant dans l’ordre d’affichage. 
        
  - VCDIR_PREV : la visionneuse doit activer le message précédent dans l’ordre d’affichage. 
        
  - VCDIR_UNREAD : la visionneuse doit activer le message non lu suivant ou précédent dans l’ordre d’affichage. 
    
_prcPosRect_
  
> [in] Pointeur vers une structure **RECT** Windows contenant la taille et la position de la fenêtre à utiliser pour afficher le message activé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été activé avec succès. 
    
S_FALSE 
  
> Le message a été activé avec succès, mais un autre type de formulaire a été ouvert dans le processus.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewContext::ActivateNext** pour modifier le message affiché à l’utilisateur. La valeur passée dans le paramètre _ulDir_ indique quel message doit être activé et, dans certains cas, pourquoi. Les indicateurs VCDIR_NEXT et VCDIR_PREVIOUS correspondent aux utilisateurs qui choisissent la commande **Suivant** ou **Précédent** dans une vue, respectivement. Ces opérations correspondent généralement au déplacement d’un message vers le haut ou vers le bas dans la liste des messages de la visionneuse de formulaires. 
  
Les indicateurs VCDIR_DELETE et VCDIR_MOVE sont définis par les méthodes [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) et [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) , respectivement. Les implémentations de ces méthodes appellent **ActivateNext** avec la direction appropriée, puis effectuent l’opération demandée sur le message si l’appel **ActivateNext** n’a pas échoué. Les visionneuses de formulaire permettent généralement aux utilisateurs de spécifier la direction à déplacer dans la liste des messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Votre implémentation [d’IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) effectue le message suivant ou précédent dans le dossier, en fonction de la valeur  _d’ulDir_, le message actuel. Une fois **activateNext** retourné, appelez [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) pour obtenir un pointeur vers le message nouvellement activé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si **ActivateNext** retourne S_FALSE, ou si aucun message actuel n’est présent, effectuez votre procédure d’arrêt normale qui doit inclure l’appel de la méthode [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) de votre formulaire. Si un message suivant ou précédent s’affiche, utilisez le rectangle de fenêtre passé dans le paramètre _prcPosRect_ pour l’afficher. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext::ActivateNext** dans cette fonction. |
   
## <a name="see-also"></a>Voir aussi

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

