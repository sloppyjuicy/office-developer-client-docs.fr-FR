---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351176"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère l'état actuel de la visionneuse. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Paramètres

 _lpulStatus_
  
> remarquer Pointeur vers un masque de réindicateur qui fournit l'état de la visionneuse. Les indicateurs suivants peuvent être définis:
    
VCSTATUS_CATEGORY 
  
> Il existe un message suivant ou précédent dans une autre catégorie. 
    
VCSTATUS_DELETE 
  
> Le formulaire permet la suppression des messages. 
    
VCSTATUS_INTERACTIVE 
  
> Le formulaire doit afficher une interface utilisateur. Si cet indicateur n'est pas défini, le formulaire doit supprimer l'affichage d'une interface utilisateur même en réponse à un verbe qui entraîne généralement l'affichage d'une interface utilisateur. 
    
VCSTATUS_MODAL 
  
> Le formulaire est modal dans la visionneuse. 
    
VCSTATUS_NEXT 
  
> Il y a un message suivant dans l'affichage. 
    
VCSTATUS_PREV 
  
> Il existe un message précédent dans l'affichage. 
    
VCSTATUS_READONLY 
  
> Le message doit être ouvert en mode lecture seule. Les opérations de suppression, d'envoi et de déplacement doivent être désactivées. 
    
VCSTATUS_UNREAD 
  
> Il y a un message non lu suivant ou précédent dans la vue.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'état de la visionneuse a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewContext:: GetViewStatus** pour déterminer s'il y a plus de messages à activer dans une vue de formulaire dans l'une ou l'autre des directions, dans le sens où une commande **suivante** active les messages, dans le sens dans lequel une commande **précédente** active les messages, ou dans les deux sens. La valeur indiquée par le paramètre _lpulStatus_ est utilisée pour déterminer si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont valides pour [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md). Si l'indicateur VCSTATUS_DELETE est défini, mais pas l'indicateur VCSTATUS_READONLY, le message peut être supprimé à l'aide de la méthode [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) . 
  
En règle générale, les formulaires désactivent les commandes de menu et les boutons s'ils ne sont pas valides pour le contexte de l'utilisateur. Une visionneuse peut alerter un formulaire à une modification de l'État en appelant sa méthode [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) . 
  
L'indicateur VCSTATUS_MODAL est défini si le formulaire doit être modal dans la fenêtre dont le descripteur est passé dans l' [IMAPIForm précédent::D overb](imapiform-doverb.md) . Si VCSTATUS_MODAL est défini, le formulaire peut utiliser le thread sur lequel l'appel de **verbe** a été effectué jusqu'à la fermeture du formulaire. Si VCSTATUS_MODAL n'est pas défini, le formulaire ne doit pas être modal dans cette fenêtre et ne doit pas utiliser le thread. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetViewStatus  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext:: GetViewStatus** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

