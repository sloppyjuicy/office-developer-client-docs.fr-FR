---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321412"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime le message actif.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Paramètres

 _pViewContext_
  
> dans Pointeur vers un objet de contexte d'affichage.
    
 _prcPosRect_
  
> dans Pointeur vers une structure [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la position et la taille de la fenêtre du formulaire actif. Le formulaire suivant affiché utilise également le rectangle de cette fenêtre. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L'opération n'est pas prise en charge par ce site de messages.
    
## <a name="remarks"></a>Remarques

Un objet Form appelle la méthode **IMAPIMessageSite::D eletemessage** pour supprimer le message actuellement affiché par le formulaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Suite au retour de **DeleteMessage**, les objets de formulaire doivent vérifier la présence d'un nouveau message, puis le faire disparaître s'il n'en existe pas. Pour déterminer si le message **DeleteMessage** a été supprimé ou déplacé vers un dossier **éléments supprimés** , un objet Form peut appeler la méthode [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) afin de déterminer si l'indicateur DELETE_IS_MOVE a été renvoyé. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si l'implémentation d'une visionneuse de formulaires de la méthode **DeleteMessage** passe au message suivant une fois qu'il a supprimé un message, l'implémentation doit appeler la méthode [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md) et passer l'indicateur VCDIR_DELETE avant d'effectuer la suppression effective. Si l'implémentation d'une visionneuse de formulaires de **DeleteMessage** déplace le message supprimé (par exemple, vers un dossier **éléments supprimés** ), l'implémentation doit enregistrer les modifications apportées au message si celui-ci a été modifié. 
  
Une implémentation type de **DeleteMessage** effectue les tâches suivantes: 
  
1. Si l'implémentation déplace le message, elle appelle la méthode [IPersistMessage:: Save](ipersistmessage-save.md) , en transmettant **null** dans le paramètre _pMessage_ et **true** dans le paramètre _fSameAsLoad_ . 
    
2. Il appelle la méthode **IMAPIViewContext:: ActivateNext,** , en transmettant l'indicateur VCDIR_DELETE dans le paramètre _ulDir_ . 
    
3. Si l'appel **ActivateNext,** échoue, il renvoie. Si **ActivateNext,** renvoie S_FALSE, il appelle la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Il supprime ou déplace le message.
    
Pour obtenir la structure **Rect** utilisée par la fenêtre d'un formulaire, appelez la fonction [GetWindowRect](https://msdn.microsoft.com/library/ms633519) de Windows. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

