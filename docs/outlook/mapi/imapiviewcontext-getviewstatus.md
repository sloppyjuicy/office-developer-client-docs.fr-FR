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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 992d51526c45334f6db3738e36994f4bb9c07c6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572255"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Récupère l’état actuel de la visionneuse. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Paramètres

 _lpulStatus_
  
> [out] Pointeur vers un masque de bits d’indicateurs fournissant l’état de la visionneuse. Les indicateurs suivants peuvent être définis :
    
VCSTATUS_CATEGORY 
  
> Il existe un message suivant ou précédent dans une autre catégorie. 
    
VCSTATUS_DELETE 
  
> Le formulaire permet aux messages à supprimer. 
    
VCSTATUS_INTERACTIVE 
  
> Le formulaire doit afficher une interface utilisateur. Si cet indicateur n’est pas défini, le formulaire doit supprimer affichant une interface utilisateur même en réponse à un verbe qui provoque généralement une interface utilisateur à afficher. 
    
VCSTATUS_MODAL 
  
> Le formulaire est modal à l’afficheur. 
    
VCSTATUS_NEXT 
  
> Il existe un message suivant dans l’affichage. 
    
VCSTATUS_PREV 
  
> Il existe un message précédent dans l’affichage. 
    
VCSTATUS_READONLY 
  
> Le message doit être ouvert en mode lecture seule. Supprimer, soumettre et déplacer des opérations doivent être désactivées. 
    
VCSTATUS_UNREAD 
  
> Il existe un message non lu suivant ou précédent dans l’affichage.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> État de l’utilisateur a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

Objets formulaire appeler la méthode **IMAPIViewContext::GetViewStatus** pour déterminer s’il existe plus de messages pour être activé en mode formulaire dans un ou les deux sens, autrement dit, dans le sens dans lequel une commande **suivant** Active les messages, dans la sens dans lequel une commande **précédente** Active les messages, ou dans les deux sens. La valeur indiquée par le paramètre _lpulStatus_ est utilisée pour déterminer si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont valides pour [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Si l’indicateur VCSTATUS_DELETE est set, mais pas l’indicateur VCSTATUS_READONLY, le message peut être supprimé à l’aide de la méthode [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) . 
  
En règle générale, formulaires désactiver les commandes de menu et les boutons si elles ne sont pas valides pour le contexte de l’utilisateur. Une visionneuse peut alerter un formulaire à un changement d’état en appelant la méthode [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) . 
  
L’indicateur VCSTATUS_MODAL est défini si le formulaire doit être modal à la fenêtre dont le descripteur est transmis dans l’appel [IMAPIForm::DoVerb](imapiform-doverb.md) antérieur. Si VCSTATUS_MODAL est défini, le formulaire peut utiliser le thread sur lequel l’appel de **DoVerb** a été effectué jusqu'à ce que le formulaire se ferme. Si VCSTATUS_MODAL n’est pas défini, le formulaire ne doit pas être modal dans cette fenêtre et ne doit pas utiliser le thread. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext::GetViewStatus** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

