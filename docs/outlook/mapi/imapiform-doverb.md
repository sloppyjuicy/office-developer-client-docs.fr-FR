---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9ea44c9ba75390f06ff12ddeed0c7b652538e07d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783784"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**S’applique à**: Outlook 
  
Exige que le formulaire exécute ce que les tâches associe un verbe spécifique.
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>Paramètres

 _iVerb_
  
> [in] Le numéro associé à un des verbes du formulaire.
    
 _lpViewContext_
  
> [in] Pointeur vers un objet de contexte de vue. Le paramètre _lpViewContext_ peut être **null**.
    
 _hwndParent_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche. Le paramètre _hwndParent_ doit être **null** si la boîte de dialogue ou fenêtre n’est pas modal. 
    
 _lprcPosRect_
  
> [in] Un pointeur vers un Win32 structure [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) qui contient la taille et la position de la fenêtre du formulaire. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le verbe a été invoqué.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Le verbe représenté par le paramètre _iVerb_ est valid, mais le formulaire ne peut pas effectuer les opérations actuellement associées. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIForm::DoVerb** pour demander que le formulaire effectuer les tâches qu’elle associe à chaque verbe prenant en charge le formulaire. 
  
Chacun des verbes pris en charge est identifiée par une valeur numérique, transmise à **DoVerb** dans le paramètre _iVerb_ . Implémentations classiques de **DoVerb** contient une instruction **switch** qui teste les valeurs valides pour le paramètre _iVerb_ pour le formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si la visionneuse de formulaire spécifie un contexte de vue dans le paramètre _lpViewContext_ , l’utiliser dans votre implémentation **DoVerb** au lieu du contexte de vue passée dans un appel précédent à la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) . Apportez toutes les modifications sont nécessaires pour vos structures de données internes et ne pas enregistrent le contexte de vue. 
  
Dans votre implémentation **DoVerb** , effectuez les tâches suivantes : 
  
- Exécuter le code est nécessaire pour le verbe qui est associé avec le paramètre _iVerb_ . 
    
- Si nécessaire, restaurez le contexte de vue d’origine.
    
- Si un numéro de verbe inconnu a été passé, retourne MAPI_E_NO_SUPPORT. Sinon, retourne un résultat basé sur la réussite ou l’échec de n’importe quel verbe a été exécuté.
    
- Fermer le formulaire. Il est toujours votre responsabilité pour fermer le formulaire après un appel de **DoVerb** . 
    
Certains verbes, telles qu’Imprimer, doivent être modales en ce qui concerne l’appel de **DoVerb** — autrement dit, l’opération indiquée doit être terminée avant l’appel de **DoVerb** retourné. 
  
Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
N’enregistrez pas la poignée dans le paramètre _hwndParent_ car, même si elle reste généralement valide jusqu'à la fin de **DoVerb**, il peut être détruit immédiatement lors du retour de l’appel.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez émettre des verbes non modal agir comme verbes modales, pointez sur une implémentation de contexte de vue qui retourne l’indicateur VCSTATUS_MODAL à partir de la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) _lpViewContext_ . 
  
Pour plus d’informations sur les verbes MAPI, voir [Verbes du formulaire](form-verbs.md). Pour plus d’informations sur la gestion des verbes OLE, voir [OLE et transfert de données](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI utilise la méthode **IMAPIForm::DoVerb** pour appeler un verbe sur un formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Formulaire verbes](form-verbs.md)

