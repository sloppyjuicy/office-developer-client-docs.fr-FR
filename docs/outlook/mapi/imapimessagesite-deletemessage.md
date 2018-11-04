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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396490"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime le message en cours.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Paramètres

 _pViewContext_
  
> [in] Pointeur vers un objet de contexte de vue.
    
 _prcPosRect_
  
> [in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la taille de la fenêtre et la position du formulaire actif. Le formulaire suivant utilise également ce rectangle de la fenêtre. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas pris en charge par ce site de message.
    
## <a name="remarks"></a>Remarques

Un objet form appelle la méthode **IMAPIMessageSite::DeleteMessage** pour supprimer le message qui affiche le formulaire actuellement. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Après le renvoi de **DeleteMessage**, objets de formulaire doivent vérifier un nouveau message et puis faire disparaître eux-mêmes si aucune n’existe. Pour déterminer si le message effectuées **DeleteMessage** a été supprimé ou déplacé vers un dossier **Éléments supprimés** , un objet de formulaire peut appeler la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) pour déterminer si l’indicateur DELETE_IS_MOVE a été renvoyée. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Si l’implémentation d’une visionneuse formulaire de la méthode **DeleteMessage** déplace le message suivant après avoir supprimé un message, l’implémentation doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) et transmettez l’indicateur VCDIR_DELETE avant d’exécuter la suppression effective. Si l’implémentation d’une visionneuse formulaire de **DeleteMessage** déplace le message supprimé (par exemple, pour un dossier **Éléments supprimés** ), l’implémentation doit enregistrer les modifications dans le message si le message a été modifié. 
  
Une implémentation classique de **DeleteMessage** effectue les tâches suivantes : 
  
1. Si l’implémentation est déplacé le message, il appelle la méthode [IPersistMessage::Save](ipersistmessage-save.md) , en passant **null** dans le paramètre _pMessage_ et **la valeur true** dans le paramètre _fSameAsLoad_ . 
    
2. Il appelle la méthode **IMAPIViewContext::ActivateNext** , en passant l’indicateur VCDIR_DELETE dans le paramètre _ulDir_ . 
    
3. Si l’appel **ActivateNext** échoue, elle renvoie. Si **ActivateNext** renvoie S_FALSE, il appelle la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Il supprime ou déplace le message.
    
Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) . 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

