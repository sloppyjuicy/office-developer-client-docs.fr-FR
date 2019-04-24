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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286627"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique qu'une modification a eu lieu dans l'état de la visionneuse de formulaires. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Paramètres

 _ulDir_
  
> dans Masque de des indicateurs qui fournit des informations sur la modification survenue dans la visionneuse et la réponse attendue dans le formulaire. Les indicateurs suivants peuvent être définis:
    
VCSTATUS_CATEGORY 
  
> Il existe un message suivant ou précédent dans une autre catégorie. 
    
VCSTATUS_INTERACTIVE 
  
> Le formulaire doit afficher une interface utilisateur. Si cet indicateur n'est pas défini, le formulaire doit supprimer l'affichage d'une interface utilisateur, même en réponse à un verbe qui entraîne généralement l'affichage d'une interface utilisateur. 
    
VCSTATUS_MODAL 
  
> Le formulaire doit être modal dans la visionneuse de formulaire. 
    
VCSTATUS_NEXT 
  
> Il y a un message suivant dans la visionneuse de formulaires. 
    
VCSTATUS_PREV 
  
> Il existe un message précédent dans la visionneuse de formulaires. 
    
VCSTATUS_READONLY 
  
> Les opérations de suppression, d'envoi et de déplacement doivent être désactivées. 
    
VCSTATUS_UNREAD 
  
> Il y a un message non lu suivant ou précédent dans la visionneuse de formulaires.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormAdviseSink:: OnChange** pour informer le formulaire des modifications apportées à l'état d'une visionneuse. En règle générale, la seule modification consiste à définir ou à désactiver l'indicateur VCSTATUS_NEXT ou VCSTATUS_PREVIOUS en fonction de la présence ou de l'absence d'un message suivant ou précédent dans la visionneuse. Par conséquent, l'objet Form active ou désactive les actions suivantes ou précédentes qu'il prend en charge. 
  
Les paramètres de VCSTATUS_MODAL et VCSTATUS_INTERACTIVE ne peuvent pas être modifiés dans un contexte d'affichage une fois qu'il a été créé.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L'implémentation spécifique de cette méthode dépend entièrement des caractéristiques du formulaire. La plupart des objets de formulaire utilisent cette méthode pour modifier leur interface utilisateur (par exemple, pour activer ou désactiver les commandes de menu ou les boutons pour qu'ils correspondent au paramètre indicateurs d'état de la visionneuse).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

