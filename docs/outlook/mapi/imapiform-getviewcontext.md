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
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783748"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**S’applique à**: Outlook 
  
Renvoie le contexte actuel de la vue pour le formulaire. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Paramètres

 _ppViewContext_
  
> [out] Pointeur vers un pointeur vers le contexte de vue du formulaire.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Contexte d’affichage actuel du formulaire a été renvoyée avec succès. 
    
S_FALSE 
  
> Il n’existe aucun contexte de vue pour le formulaire.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appellent **GetViewContext** pour obtenir un pointeur vers le contexte de vue établi dans un appel précédent à [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Si aucun appel précédent n’a été effectuée pour **SetViewContext**, **GetViewContext** définit _ppViewContext_ sur NULL. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Copiez le pointeur de contexte de vue de votre formulaire dans le pointeur passé par la visionneuse de formulaire appelant dans le paramètre _ppViewContext_ . Si le formulaire ne dispose pas d’un contexte de vue, _ppViewContext_ la valeur NULL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la méthode **IMAPIForm::GetViewContext** pour vérifier si un formulaire possède un contexte de vue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

