---
title: IMAPIMessageSiteDeleteMessage
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIMessageSiteDeleteMessage, qui supprime le message actuel.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
ms.openlocfilehash: 1b74a47946b46e3d58382c14e240b6aa1828b870
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816324"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime le message actuel.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Paramètres

 _pViewContext_
  
> [in] Pointeur vers un objet de contexte d’affichage.
    
 _prcPosRect_
  
> [in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la taille et la position de la fenêtre du formulaire actuel. Le formulaire suivant affiché utilise également ce rectangle de fenêtre. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas prise en charge par ce site de message.
    
## <a name="remarks"></a>Remarques

Un objet de formulaire appelle la méthode **IMAPIMessageSite::D eleteMessage** pour supprimer le message que le formulaire affiche actuellement. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Après le retour de **DeleteMessage, les** objets de formulaire doivent rechercher un nouveau message, puis se faire ignorer s’il n’en existe aucun. Pour déterminer si le message **DeleteMessage** a été supprimé ou déplacé vers un dossier **Éléments supprimés** , un objet de formulaire peut appeler la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) pour déterminer si l’indicateur DELETE_IS_MOVE a été retourné. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si l’implémentation de la méthode **DeleteMessage** par une visionneuse de formulaires passe au message suivant après la suppression d’un message, l’implémentation doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) et passer l’indicateur VCDIR_DELETE avant d’effectuer la suppression réelle. Si l’implémentation de **DeleteMessage** par une visionneuse de formulaires déplace le message supprimé (par exemple, vers un dossier **Éléments supprimés** ), l’implémentation doit enregistrer les modifications apportées au message si le message a été modifié. 
  
Une implémentation classique de **DeleteMessage** effectue les tâches suivantes : 
  
1. Si l’implémentation déplace le message, elle appelle la méthode [IPersistMessage::Save](ipersistmessage-save.md) , en passant **null** dans le paramètre _pMessage_ et **true** dans le paramètre _fSameAsLoad_ . 
    
2. Il appelle la méthode **IMAPIViewContext::ActivateNext** , en passant l’indicateur VCDIR_DELETE dans le paramètre _ulDir_ . 
    
3. Si l’appel **ActivateNext** échoue, il retourne. Si **ActivateNext** retourne S_FALSE, il appelle la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Il supprime ou déplace le message.
    
Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la Windows fonction [GetWindowRect](https://msdn.microsoft.com/library/ms633519). 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, consultez [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Non implémenté. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

