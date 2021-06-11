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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430902"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le contexte d’affichage actuel du formulaire. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameters

 _ppViewContext_
  
> [out] Pointeur vers un pointeur vers le contexte d’affichage du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contexte d’affichage actuel du formulaire a été renvoyé avec succès. 
    
S_FALSE 
  
> Il n’existe aucun contexte d’affichage pour le formulaire.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire **appellent GetViewContext** pour obtenir un pointeur vers le contexte d’affichage établi dans un appel précédent à [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Si aucun appel préalable n’a été effectué sur **SetViewContext,** **GetViewContext** définit  _ppViewContext_ sur NULL. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Copiez le pointeur de contexte d’affichage de votre formulaire dans le pointeur transmis par la visionneuse de formulaire appelant dans le _paramètre ppViewContext._ Si le formulaire ne comporte pas de contexte d’affichage, définissez  _ppViewContext_ sur NULL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la **méthode IMAPIForm::GetViewContext** pour vérifier si un formulaire possède un contexte d’affichage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

