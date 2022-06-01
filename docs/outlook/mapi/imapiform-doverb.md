---
title: IMAPIFormDoVerb
description: Décrit les paramètres, la valeur de retour et les remarques pour IMAPIFormDoVerb, qui demande que le formulaire effectue toutes les tâches qu’il associe à un verbe spécifique.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
ms.openlocfilehash: 351ae0ebd25c9601bbda06891592e7fd50e3cabb
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816870"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le formulaire effectue toutes les tâches associées à un verbe spécifique.
  
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
  
> [in] Nombre associé à l’un des verbes du formulaire.
    
 _lpViewContext_
  
> [in] Pointeur vers un objet de contexte d’affichage. Le paramètre  _lpViewContext_ peut être **null**.
    
 _hwndParent_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. Le paramètre  _hwndParent_ doit être **null** si la boîte de dialogue ou la fenêtre n’est pas modale. 
    
 _lprcPosRect_
  
> [in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32 qui contient la taille et la position de la fenêtre du formulaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le verbe a été appelé avec succès.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Le verbe représenté par le paramètre  _iVerb_ est valide, mais le formulaire ne peut pas effectuer les opérations actuellement associées. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent la méthode **IMAPIForm::D oVerb** pour demander au formulaire d’effectuer les tâches qu’il associe à chaque verbe pris en charge par le formulaire. 
  
Chacun des verbes pris en charge est identifié par une valeur numérique, passée à **DoVerb** dans le paramètre _iVerb_ . Les implémentations classiques de **DoVerb** contiennent une instruction **switch** qui teste les valeurs valides pour le paramètre  _iVerb_ du formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si la visionneuse de formulaires spécifie un contexte d’affichage dans le paramètre _lpViewContext_ , utilisez-le dans votre implémentation **DoVerb** au lieu du contexte d’affichage passé dans un appel précédent à la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) . Apportez les modifications nécessaires à vos structures de données internes et n’enregistrez pas le contexte d’affichage. 
  
Effectuez les tâches suivantes dans votre implémentation **DoVerb** : 
  
- Exécutez le code nécessaire pour le verbe particulier associé au paramètre  _iVerb_ . 
    
- Si nécessaire, restaurez le contexte d’affichage d’origine.
    
- Si un nombre de verbes inconnu a été transmis, retournez MAPI_E_NO_SUPPORT. Sinon, retournez un résultat en fonction de la réussite ou de l’échec du verbe qui a été exécuté.
    
- Fermez le formulaire. Il est toujours de votre responsabilité de fermer le formulaire une fois qu’un appel **DoVerb** est terminé. 
    
Certains verbes, tels que Print, doivent être modaux en ce qui concerne l’appel **DoVerb** , c’est-à-dire que l’opération indiquée doit être terminée avant le retour de l’appel **DoVerb** . 
  
Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction [GetWindowRect](https://msdn.microsoft.com/library/ms633519) . 
  
N’enregistrez pas le handle dans le paramètre _hwndParent_ , car, bien qu’il reste généralement valide jusqu’à la fin de **DoVerb**, il peut être détruit immédiatement au retour de l’appel.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez faire en sorte que les verbes non modaux agissent comme des verbes modaux en pointant  _lpViewContext_ vers une implémentation de contexte de vue qui retourne l’indicateur VCSTATUS_MODAL à partir de sa méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) . 
  
Pour plus d’informations sur les verbes dans MAPI, consultez [Verbes de formulaire](form-verbs.md). Pour plus d’informations sur la façon dont les verbes sont gérés dans OLE, consultez [OLE et Transfert de données](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI utilise la méthode **IMAPIForm::D oVerb** pour appeler un verbe sur un formulaire. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Verbes de formulaire](form-verbs.md)

