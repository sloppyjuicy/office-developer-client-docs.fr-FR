---
title: IMAPIViewContextGetViewStatus
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b8549c2abbad33baf38312f0d803f1f6f3a8244
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579893"
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
  
> [out] Pointeur vers un masque de bits d’indicateurs fournissant l’état de la visionneuse. Les indicateurs suivants peuvent être définies :
    
VCSTATUS_CATEGORY 
  
> Il existe un message suivant ou précédent dans une autre catégorie. 
    
VCSTATUS_DELETE 
  
> Le formulaire permet la suppression des messages. 
    
VCSTATUS_INTERACTIVE 
  
> Le formulaire doit afficher une interface utilisateur. Si cet indicateur n’est pas définie, le formulaire doit supprimer l’affichage d’une interface utilisateur, même en réponse à un verbe qui entraîne généralement l’affichage d’une interface utilisateur. 
    
VCSTATUS_MODAL 
  
> Le formulaire est modal pour la visionneuse. 
    
VCSTATUS_NEXT 
  
> L’affichage affiche un message suivant. 
    
VCSTATUS_PREV 
  
> L’affichage affiche un message précédent. 
    
VCSTATUS_READONLY 
  
> Le message doit être ouvert en mode lecture seule. Les opérations de suppression, d’soumission et de déplacement doivent être désactivées. 
    
VCSTATUS_UNREAD 
  
> L’affichage affiche un message non lu suivant ou précédent.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état de la visionneuse a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

Les objets Form appellent la méthode **IMAPIViewContext::GetViewStatus** pour déterminer s’il existe d’autres messages à activer dans une vue de formulaire dans l’une ou l’autre direction ou dans les deux sens, dans la direction dans laquelle une commande **Next** active les messages, dans la direction dans laquelle une commande Précédente active les messages ou dans les deux sens.  La valeur pointée par le paramètre  _lpulStatus_ permet de déterminer si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont valides pour [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Si l’indicateur VCSTATUS_DELETE est définie, mais pas l’indicateur VCSTATUS_READONLY, le message peut être supprimé à l’aide de la méthode [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md) 
  
En règle générale, les formulaires désactivent les commandes de menu et les boutons s’ils ne sont pas valides pour le contexte de la visionneuse. Une visionneuse peut alerter un formulaire d’un changement d’état en appelant sa méthode [IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md) 
  
L VCSTATUS_MODAL est définie si le formulaire doit être modal pour la fenêtre dont le handle est transmis dans l’appel [IMAPIForm::D oVerb](imapiform-doverb.md) précédent. Si VCSTATUS_MODAL est définie, le formulaire peut utiliser le thread sur lequel l’appel **DoVerb a** été effectué jusqu’à la fermeture du formulaire. Si VCSTATUS_MODAL n’est pas définie, le formulaire ne doit pas être modal dans cette fenêtre et ne doit pas utiliser le thread. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implémente **la méthode IMAPIViewContext::GetViewStatus** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

