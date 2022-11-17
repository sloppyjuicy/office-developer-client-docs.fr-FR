---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 91c6a61acefe4c18e889689fc8d7ca7054d833d1
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463085"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit un contexte d’affichage pour le formulaire. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Paramètres

 _pViewContext_
  
> [in] Pointeur vers le nouveau contexte d’affichage du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contexte d’affichage a été correctement définie.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent **la méthode IMAPIForm::SetViewContext** pour établir un contexte d’affichage de formulaire particulier comme étant actuel. Un formulaire ne peut avoir qu’un contexte d’affichage à la fois. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La plupart des serveurs de formulaire **implémentent SetViewContext** à l’aide de l’algorithme suivant : 
  
- Si un contexte d’affichage existe déjà pour le formulaire, annulez l’inscription du formulaire en appelant la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) avec **la valeur null** dans le paramètre _pmnvs_ , puis appelez la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du contexte d’affichage pour décrémenter son nombre de références. 
    
- Si le nouveau contexte d’affichage n’est pas **null**, appelez **IMAPIViewContext::SetAdviseSink** à l’aide du paramètre  _pViewContext_ pour configurer un nouveau sink de conseil d’affichage. 
    
- Si le nouveau contexte d’affichage n’est pas **null**, appelez la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) pour déterminer les indicateurs d’état qui ont été définies. 
    
- Si le nouveau contexte d’affichage n’est pas **null**, stockez-le et appelez sa méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) pour incrémenter son nombre de références. 
    
- Mettez à jour tous les éléments de l’interface utilisateur qui dépendent du contexte d’affichage. 
    
Selon les indicateurs d’état renvoyés par **IMAPIViewContext::GetViewStatus**, **SetViewContext** peut également effectuer d’autres actions. Par exemple, si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont renvoyés, **SetViewContext** peut activer les boutons Suivant et Précédent pour  le nouveau  contexte d’affichage. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI utilise **la méthode IMAPIForm::SetViewContext** pour définir le contexte d’affichage de MFCMAPI sur le formulaire avant l’affichage du formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

