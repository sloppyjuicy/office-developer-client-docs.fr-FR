---
title: IMAPIFormGetViewContext
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IMAPIFormGetViewContext, qui retourne le contexte d’affichage actuel du formulaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
ms.openlocfilehash: bbaba7ef07b9fc20a4deb5d8941292395751130e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816359"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne le contexte d’affichage actuel du formulaire. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Paramètres

 _ppViewContext_
  
> [out] Pointeur vers un pointeur vers le contexte d’affichage du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contexte d’affichage actuel du formulaire a été retourné avec succès. 
    
S_FALSE 
  
> Il n’existe aucun contexte d’affichage pour le formulaire.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent **GetViewContext** pour obtenir un pointeur vers le contexte d’affichage établi dans un appel précédent à [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Si aucun appel précédent n’a été passé à **SetViewContext**, **GetViewContext** définit  _ppViewContext_ sur NULL. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Copiez le pointeur de contexte d’affichage de votre formulaire dans le pointeur transmis par la visionneuse de formulaires appelant dans le paramètre _ppViewContext_ . Si le formulaire n’a pas de contexte d’affichage,  _définissez ppViewContext_ sur NULL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la méthode **IMAPIForm::GetViewContext** pour vérifier si un formulaire a un contexte d’affichage. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

