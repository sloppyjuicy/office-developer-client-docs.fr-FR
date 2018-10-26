---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588502"
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
  
> [in] Indicateurs d’état en donnant des informations sur le message à activer. Paramètres de l’indicateur valides sont :
    
  - VCDIR_CATEGORY : La visionneuse doit activer un message dans une autre catégorie de l’affichage. Le message doit être activé est la suivante : 
        
    - Le premier message dans la catégorie de vue suivante si cet indicateur est ed **ou**avec VCDIR_NEXT. 
        
    - Le dernier message de la catégorie de vue précédente si cet indicateur est **liées avec VCDIR_PREV**et à la catégorie précédente est développé. 
        
    - Le premier message dans la catégorie de vue précédente si cet indicateur est **liées avec VCDIR_PREV**et de la catégorie précédente n’est pas développé. Dans ce cas, la catégorie précédente subit extension automatique. 
        
  - VCDIR_DELETE : La visionneuse doit activer le message suivant ou précédent, car le message en cours a été supprimé. 
        
  - VCDIR_MOVE : La visionneuse doit activer le message suivant ou précédent, car le message en cours a été déplacé. 
        
  - VCDIR_NEXT : La visionneuse doit activer le message suivant dans l’ordre d’affichage. 
        
  - VCDIR_PREV : La visionneuse doit activer le message précédent dans l’ordre d’affichage. 
        
  - VCDIR_UNREAD : La visionneuse doit activer le message non lu suivant ou précédent dans l’ordre d’affichage. 
    
_prcPosRect_
  
> [in] Pointeur vers un **RECT** Windows structure contenant la taille et la position de la fenêtre à utiliser pour afficher le message activé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été activé avec succès. 
    
S_FALSE 
  
> Le message a été activé avec succès, mais un autre type de formulaire a été ouvert dans le processus.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIViewContext::ActivateNext** pour modifier le message affiché à l’utilisateur. La valeur passée dans le paramètre _ulDir_ indique que le message doit être activé et, dans certains cas, pourquoi. Les indicateurs VCDIR_NEXT et VCDIR_PREVIOUS correspondent aux utilisateurs de choisir la commande **suivant** ou **précédent** dans un affichage, respectivement. Ces opérations correspondent généralement à un déplacement haut ou vers le bas d’un message dans la liste de l’utilisateur du formulaire des messages. 
  
Les indicateurs VCDIR_DELETE et VCDIR_MOVE sont définis par les [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) et les méthodes de [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) , respectivement. Implémentations des méthodes suivantes appelez **ActivateNext** avec le sens approprié, puis effectuez l’opération demandée dans le message si l’appel **ActivateNext** sans erreur. Formulaire permettent généralement aux utilisateurs de spécifier le sens de déplacement dans la liste des messages. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Votre implémentation de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) rend le message suivant ou précédent dans le dossier, selon la valeur _ulDir_, le message en cours. Une fois **ActivateNext** renvoie, appelez [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) pour obtenir un pointeur vers le nouveau message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si **ActivateNext** renvoie S_FALSE, ou si un message en cours n’est pas présent, effectuez la procédure d’arrêt normal qui doit inclure l’appel de méthode de [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) de votre formulaire. Si un message précédent ou suivant est affiché, utilisez le rectangle de fenêtre passé dans le paramètre _prcPosRect_ pour l’afficher. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext::ActivateNext** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

