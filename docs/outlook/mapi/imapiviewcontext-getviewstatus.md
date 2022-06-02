---
title: IMAPIViewContextGetViewStatus
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIViewContextGetViewStatus, qui récupère l’état actuel de la visionneuse.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
ms.openlocfilehash: 3fbe8be2a79634d5abcfc6b7ed8a940af59d7a53
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827771"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère l’état actuel de la visionneuse. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Paramètres

 _lpulStatus_
  
> [out] Pointeur vers un masque de bits d’indicateurs fournissant l’état de la visionneuse. Les indicateurs suivants peuvent être définis :
    
VCSTATUS_CATEGORY 
  
> Il existe un message suivant ou précédent dans une autre catégorie. 
    
VCSTATUS_DELETE 
  
> Le formulaire permet de supprimer des messages. 
    
VCSTATUS_INTERACTIVE 
  
> Le formulaire doit afficher une interface utilisateur. Si cet indicateur n’est pas défini, le formulaire doit supprimer l’affichage d’une interface utilisateur même en réponse à un verbe qui provoque généralement l’affichage d’une interface utilisateur. 
    
VCSTATUS_MODAL 
  
> Le formulaire est modal pour la visionneuse. 
    
VCSTATUS_NEXT 
  
> Un message suivant s’affiche dans la vue. 
    
VCSTATUS_PREV 
  
> Il existe un message précédent dans la vue. 
    
VCSTATUS_READONLY 
  
> Le message doit être ouvert en mode lecture seule. Les opérations de suppression, d’envoi et de déplacement doivent être désactivées. 
    
VCSTATUS_UNREAD 
  
> Il existe un message non lu suivant ou précédent dans la vue.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état de la visionneuse a été retourné avec succès.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewContext::GetViewStatus** pour déterminer si d’autres messages doivent être activés dans un affichage formulaire dans l’une ou l’autre des directions, c’est-à-dire dans la direction dans laquelle une commande **Next** active les messages, dans la direction dans laquelle une commande **Précédente** active les messages, ou dans les deux sens. La valeur pointée par le paramètre  _lpulStatus_ est utilisée pour déterminer si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont valides pour [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Si l’indicateur VCSTATUS_DELETE est défini, mais pas l’indicateur VCSTATUS_READONLY, le message peut être supprimé à l’aide de la méthode [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) . 
  
En règle générale, les formulaires désactivent les commandes de menu et les boutons s’ils ne sont pas valides pour le contexte de la visionneuse. Une visionneuse peut alerter un formulaire d’un changement d’état en appelant sa méthode [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) . 
  
L’indicateur VCSTATUS_MODAL est défini si le formulaire doit être modal pour la fenêtre dont le handle est passé dans l’appel [IMAPIForm::D oVerb](imapiform-doverb.md) précédent. Si VCSTATUS_MODAL est défini, le formulaire peut utiliser le thread sur lequel l’appel **DoVerb** a été effectué jusqu’à ce que le formulaire se ferme. Si VCSTATUS_MODAL n’est pas défini, le formulaire ne doit pas être modal pour cette fenêtre et ne doit pas utiliser le thread. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext::GetViewStatus** dans cette fonction. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

