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
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329455"
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
  
> dans Nombre associé à l'un des verbes du formulaire.
    
 _lpViewContext_
  
> dans Pointeur vers un objet de contexte d'affichage. Le paramètre _lpViewContext_ peut être **null**.
    
 _hwndParent_
  
> dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche. Le paramètre _hwndParent_ doit être **null** si la boîte de dialogue ou la fenêtre n'est pas modale. 
    
 _lprcPosRect_
  
> dans Pointeur vers une structure [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32 qui contient la taille et la position de la fenêtre du formulaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le verbe a été invoqué.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Le verbe représenté par le paramètre _iVerb_ est valide, mais le formulaire ne peut pas exécuter les opérations qui lui sont actuellement associées. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIForm::D overb** pour demander au formulaire d'effectuer les tâches qu'il associe à chaque verbe pris en charge par le formulaire. 
  
Chacun des verbes pris en charge est identifié par une valeur numérique, passée à **DoVerb** dans le paramètre _iVerb_ . Les implémentations typiques de **DoVerb** contiennent une instruction **switch** qui teste les valeurs valides pour le paramètre _iVerb_ du formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si la visionneuse de formulaires spécifie un contexte d'affichage dans le paramètre _lpViewContext_ , utilisez-la dans votre implémentation de **DoVerb** au lieu du contexte d'affichage passé dans un appel précédent à la méthode [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) . Effectuez toutes les modifications nécessaires à vos structures de données internes et n'enregistrez pas le contexte d'affichage. 
  
Effectuez les tâches suivantes dans votre implémentation de **DoVerb** : 
  
- Exécutez le code nécessaire pour le verbe particulier associé au paramètre _iVerb_ . 
    
- Si nécessaire, restaurez le contexte d'affichage d'origine.
    
- Si un numéro de verbe inconnu a été transmis, renvoyer MAPI_E_NO_SUPPORT. Sinon, retourner un résultat en fonction de la réussite ou de l'échec de tout verbe exécuté.
    
- Fermez le formulaire. Il s'agit toujours de votre responsabilité de fermer le formulaire une fois qu'un appel de **verbe** est terminé. 
    
Certains verbes, tels que Print, doivent être modaux par rapport à l'appel de **verbe** , c'est-à-dire que l'opération indiquée doit être terminée avant le retour de l'appel de **verbe** . 
  
Pour obtenir la structure **Rect** utilisée par la fenêtre d'un formulaire, appelez la fonction [GetWindowRect](https://msdn.microsoft.com/library/ms633519) . 
  
N'enregistrez pas le handle dans le paramètre _hwndParent_ car, bien qu'il reste généralement valide jusqu'à la fin de la **réverbération**, il peut être détruit immédiatement lors du retour de l'appel.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez créer des verbes non modaux qui agissent comme des verbes modaux en pointant _lpViewContext_ vers une implémentation de contexte d'affichage qui renvoie l'indicateur VCSTATUS_MODAL à partir de sa méthode [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) . 
  
Pour plus d'informations sur les verbes dans MAPI, consultez la rubrique verbes de [formulaire](form-verbs.md). Pour plus d'informations sur la façon dont les verbes sont gérés dans OLE, consultez la rubrique [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: CallDoVerb  <br/> |MFCMAPI utilise la méthode **IMAPIForm::D overb** pour appeler un verbe sur un formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Verbes de formulaire](form-verbs.md)

