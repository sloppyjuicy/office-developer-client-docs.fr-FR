---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783751"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**S’applique à**: Outlook 
  
Ferme le formulaire.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Paramètres

 _ulSaveOptions_
  
> [in] Une valeur qui détermine comment ou si les données du formulaire sont enregistrées avant la fermeture du formulaire. Vous pouvez d�finir un des indicateurs suivants :
    
SAVEOPTS_NOSAVE 
  
> Les données de formulaire ne doivent pas être enregistrées.
    
SAVEOPTS_PROMPTSAVE 
  
> L’utilisateur doit être invité à enregistrer des données modifiées dans l’écran.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Les données de formulaire doivent être enregistrées si elles ont changé depuis le dernier enregistrement. Si aucune interface utilisateur n’est affichée, le formulaire peut passer éventuellement à l’aide de la fonctionnalité pour l’option SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le formulaire a été fermé.
    
E_UNEXPECTED 
  
> Le formulaire a été fermé déjà par un appel précédent à **ShutdownForm**.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIForm::ShutdownForm** pour fermer un formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Dans votre implémentation de **ShutdownForm**, effectuez les tâches suivantes :
  
1. Vérifiez qu’une visionneuse n’a pas déjà appelée **ShutdownForm**et retourner E_UNEXPECTED si elle a. Bien qu’il s’agit probablement pas, vous devez vérifier.
    
2. Appelez la méthode de [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) de votre formulaire afin que le stockage pour le formulaire et les structures de données internes restent disponibles que le traitement est terminé. 
    
3. Déterminer s’il existe des modifications non enregistrées pour les données du formulaire. Enregistrer les données non enregistrées en fonction de la façon dont le paramètre _ulSaveOptions_ est défini en appelant la méthode [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) de votre la visionneuse. 
    
4. Détruire la fenêtre de l’interface utilisateur de votre formulaire.
    
5. Libérer le message et les objets du site de votre formulaire en appelant leurs méthodes [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . 
    
6. Avertir inscrits toutes les visionneuses de l’arrêt en attente en appelant leurs méthodes [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) . 
    
7. Appelez la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) pour annuler l’inscription de votre formulaire de notification en définissant le pointeur du récepteur advise sur **null**.
    
8. Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire des propriétés de votre formulaire. 
    
9. Appelez la méthode **IUnknown::Release** de votre formulaire, correspondant à l’appel de **AddRef** effectuée à l’étape 2. 
    
10. Elles retournent S_OK.
    
> [!NOTE]
> Une fois ces opérations terminées, les méthodes sur l’objet form qui peut être appelée uniquement valides sont celles de l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque **ShutdownForm** renvoie, indépendamment de si elle renvoie une erreur, relâchez le formulaire en appelant la méthode **IUnknown::Release** . Vous pouvez ignorer les erreurs retournées par **ShutdownForm**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

