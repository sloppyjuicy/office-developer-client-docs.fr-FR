---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
ms.openlocfilehash: 225624fc81655b9f5a6afcf1ffe9d4a66beffa54
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382103"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ferme le formulaire.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Paramètres

 _ulSaveOptions_
  
> [in] Valeur qui contrôle comment ou si les données du formulaire sont enregistrées avant la fermeture du formulaire. Vous pouvez d�finir un des indicateurs suivants :
    
SAVEOPTS_NOSAVE 
  
> Les données de formulaire ne doivent pas être enregistrées.
    
SAVEOPTS_PROMPTSAVE 
  
> L’utilisateur doit être invité à enregistrer les données modifiées dans le formulaire.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Les données de formulaire doivent être enregistrées si elles ont été modifiées depuis le dernier sauvegarde. Si aucune interface utilisateur n’est affichée, le formulaire peut éventuellement basculer vers l’utilisation de la fonctionnalité pour l SAVEOPTS_NOSAVE’option.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a été fermé.
    
E_UNEXPECTED 
  
> Le formulaire a déjà été fermé par un appel préalable **à ShutdownForm**.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire **appellent la méthode IMAPIForm::ShutdownForm** pour fermer un formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Effectuez les tâches suivantes dans votre implémentation **de ShutdownForm** :
  
1. Vérifiez qu’une visionneuse n’a pas encore appelé **ShutdownForm** et E_UNEXPECTED si c’est le cas. Bien que cela soit peu probable, vous devez vérifier.
    
2. Appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de votre formulaire afin que le stockage du formulaire et de toutes les structures de données internes restent disponibles jusqu’à la fin du traitement. 
    
3. Déterminez s’il existe des modifications non apportées aux données du formulaire. Enregistrez les données non enregistrer en fonction de la façon dont le paramètre  _ulSaveOptions_ est définie en appelant la méthode [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) de votre visionneuse. 
    
4. Détruire la fenêtre d’interface utilisateur de votre formulaire.
    
5. Release your form’s message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods. 
    
6. Informez tous les utilisateurs inscrits de l’arrêt en attente en appelant leurs méthodes [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) . 
    
7. Appelez [la méthode IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) pour annuler l’inscription de votre formulaire pour la notification en réglant le pointeur de réception de notification sur **null**.
    
8. Appelez la [fonction MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour les propriétés de votre formulaire. 
    
9. Appelez la méthode **IUnknown::Release** de votre formulaire, correspondant à l’appel **AddRef** effectué à l’étape 2. 
    
10. Elles retournent S_OK.
    
> [!NOTE]
> Une fois ces actions terminées, les seules méthodes valides sur l’objet de formulaire qui peuvent être appelées sont celles de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **ShutdownForm renvoie** , qu’il renvoie ou non une erreur, relâchez le formulaire en appelant sa méthode **IUnknown::Release** . Vous pouvez ignorer en toute sécurité les erreurs renvoyées par **ShutdownForm**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

