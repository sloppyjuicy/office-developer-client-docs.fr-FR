---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329458"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le contexte d'affichage actuel du formulaire. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Paramètres

 _ppViewContext_
  
> remarquer Pointeur vers un pointeur vers le contexte d'affichage du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contexte d'affichage actuel du formulaire a été renvoyé. 
    
S_FALSE 
  
> Il n'existe pas de contexte d'affichage pour le formulaire.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent **GetViewContext** pour obtenir un pointeur vers le contexte d'affichage établi dans un appel précédent à [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md). Si aucun appel antérieur n'a été effectué vers **SetViewContext**, **GetViewContext** définit _ppViewContext_ sur null. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Copiez le pointeur de contexte de vue de votre formulaire dans le pointeur transmis par la visionneuse de formulaire appelant dans le paramètre _ppViewContext_ . Si le formulaire n'a pas de contexte d'affichage, affectez la valeur NULL à _ppViewContext_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la méthode **IMAPIForm:: GetViewContext** pour vérifier si un formulaire possède un contexte d'affichage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

