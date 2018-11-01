---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576679"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaire. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Paramètres

 _ulDir_
  
> [in] Masque de bits d’indicateurs qui fournit des informations sur la modification s’est produite dans la visionneuse et la réponse attendue dans le formulaire. Les indicateurs suivants peuvent être définis :
    
VCSTATUS_CATEGORY 
  
> Il existe un message suivant ou précédent dans une autre catégorie. 
    
VCSTATUS_INTERACTIVE 
  
> Le formulaire doit afficher une interface utilisateur. Si cet indicateur n’est pas défini, le formulaire doit supprimer l’affichage d’une interface utilisateur, même en réponse à un verbe qui provoque généralement une interface utilisateur à afficher. 
    
VCSTATUS_MODAL 
  
> Le formulaire est modal à la visionneuse de formulaire. 
    
VCSTATUS_NEXT 
  
> Il existe un message suivant dans la visionneuse de formulaire. 
    
VCSTATUS_PREV 
  
> Il existe un message précédent dans la visionneuse de formulaire. 
    
VCSTATUS_READONLY 
  
> Supprimer, soumettre et déplacer des opérations doivent être désactivées. 
    
VCSTATUS_UNREAD 
  
> Il existe un message non lu suivant ou précédent dans la visionneuse de formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormAdviseSink::OnChange** pour notifier le formulaire sur un changement d’état d’un utilisateur donné. En règle générale, la seule modification est définir ou effacer l’indicateur VCSTATUS_NEXT ou VCSTATUS_PREVIOUS en fonction de la présence ou non d’un message suivant ou précédent dans la visionneuse. En conséquence, l’objet form puis l’Active ou désactive toutes les actions suivante ou précédentes que pris en charge. 
  
Impossible de modifier les paramètres de VCSTATUS_MODAL et VCSTATUS_INTERACTIVE dans un contexte de vue après que qu’elle a été créée.
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

L’implémentation de cette méthode est complètement varie selon les caractéristiques du formulaire. La plupart des objets de formulaire utiliser cette méthode pour modifier leur interface utilisateur (par exemple, pour activer ou désactiver les commandes de menu ou les boutons pour correspondre au paramètre d’indicateurs de statut visionneuse).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

