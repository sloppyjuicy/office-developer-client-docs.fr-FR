---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350945"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit un contexte d'affichage pour le formulaire. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Paramètres

 _pViewContext_
  
> dans Pointeur vers le nouveau contexte d'affichage du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contexte d'affichage a été correctement défini.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIForm:: SetViewContext** pour établir un contexte de mode formulaire particulier comme étant en cours. Un formulaire ne peut avoir qu'un seul contexte d'affichage à la fois. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La plupart des serveurs de formulaire implémentent **SetViewContext** à l'aide de l'algorithme suivant: 
  
- S'il existe déjà un contexte de vue pour le formulaire, annulez l'enregistrement du formulaire en appelant la méthode [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) avec **null** dans le paramètre _pmnvs_ , puis appelez la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du contexte d'affichage. méthode pour décrémenter son décompte de références. 
    
- Si le nouveau contexte d'affichage n'a pas la **valeur null**, appelez **IMAPIViewContext:: SetAdviseSink** à l'aide du paramètre _pViewContext_ pour configurer un nouveau récepteur de notifications d'affichage. 
    
- Si le nouveau contexte d'affichage n'a pas la **valeur null**, appelez la méthode [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) pour déterminer quels indicateurs d'État ont été définis. 
    
- Si le nouveau contexte d'affichage n'a pas la **valeur null**, stockez-le et appelez sa méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) pour incrémenter son décompte de références. 
    
- Mettez à jour les éléments d'interface utilisateur qui dépendent du contexte d'affichage. 
    
En fonction des indicateurs d'État renvoyés par **IMAPIViewContext:: GetViewStatus**, **SetViewContext** peut également effectuer d'autres actions. Par exemple, si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont renvoyés, **SetViewContext** pouvez activer les boutons **suivant** et **précédent** pour le nouveau contexte d'affichage. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI utilise la méthode **IMAPIForm:: SetViewContext** pour définir le contexte d'affichage de MFCMAPI sur le formulaire avant l'affichage du formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

