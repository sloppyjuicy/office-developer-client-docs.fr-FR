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
ms.openlocfilehash: c1ba49ba1b4deacb684da1411d86ebd4dd19e63f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783759"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**S’applique à**: Outlook 
  
Établissement d’un contexte de vue pour le formulaire. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Paramètres

 _pViewContext_
  
> [in] Pointeur vers le nouveau contexte de vue pour le formulaire.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le contexte d’affichage a été défini.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode de **IMAPIForm::SetViewContext** pour établir un contexte de vue de formulaire donné comme actif. Un formulaire peut avoir qu’un seul contexte de vue à la fois. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

La plupart des serveurs de formulaire implémenter **SetViewContext** à l’aide de l’algorithme suivant : 
  
- Si un contexte de vue existe déjà pour le formulaire, annuler l’inscription du formulaire en appelant la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) avec la **valeur null** dans le paramètre _pmnvs_ et ensuite appeler [IUnknown::Release du contexte vue](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) méthode décrémente le décompte de références. 
    
- Si le contexte d’affichage n’est pas **null**, l’appel **IMAPIViewContext::SetAdviseSink** en utilisant le paramètre _pViewContext_ pour définir un nouvel affichage de notification récepteur. 
    
- Si le contexte d’affichage n’est pas **null**, appelez la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) pour déterminer les indicateurs d’état ont été définies. 
    
- Si le contexte d’affichage n’est pas **null**, stocker, appelez la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) pour incrémenter son décompte de références. 
    
- Mettre à jour les éléments d’interface utilisateur qui dépendent du contexte d’affichage. 
    
Selon les indicateurs d’état renvoyés par **IMAPIViewContext::GetViewStatus**, **SetViewContext** peut également exécuter d’autres actions. Par exemple, si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont renvoyés, **SetViewContext** peut activer les boutons **suivant** et **précédent** pour le contexte d’affichage. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI utilise la méthode **IMAPIForm::SetViewContext** pour définir le contexte de vue de MFCMAPI sur le formulaire avant que le formulaire s’affiche.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

