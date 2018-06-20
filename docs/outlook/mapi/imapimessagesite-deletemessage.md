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
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783828"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**S’applique à**: Outlook 
  
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
  
> [in] Pointeur vers une structure [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) qui contient la taille de la fenêtre et la position du formulaire actif. Le formulaire suivant utilise également ce rectangle de la fenêtre. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas pris en charge par ce site de message.
    
## <a name="remarks"></a>Remarques

Un objet form appelle la méthode **IMAPIMessageSite::DeleteMessage** pour supprimer le message qui affiche le formulaire actuellement. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Après le renvoi de **DeleteMessage**, objets de formulaire doivent vérifier un nouveau message et puis faire disparaître eux-mêmes si aucune n’existe. Pour déterminer si le message effectuées **DeleteMessage** a été supprimé ou déplacé vers un dossier **Éléments supprimés** , un objet de formulaire peut appeler la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) pour déterminer si l’indicateur DELETE_IS_MOVE a été renvoyée. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si l’implémentation d’une visionneuse formulaire de la méthode **DeleteMessage** déplace le message suivant après avoir supprimé un message, l’implémentation doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) et transmettez l’indicateur VCDIR_DELETE avant d’exécuter la suppression effective. Si l’implémentation d’une visionneuse formulaire de **DeleteMessage** déplace le message supprimé (par exemple, pour un dossier **Éléments supprimés** ), l’implémentation doit enregistrer les modifications dans le message si le message a été modifié. 
  
Une implémentation classique de **DeleteMessage** effectue les tâches suivantes : 
  
1. Si l’implémentation est déplacé le message, il appelle la méthode [IPersistMessage::Save](ipersistmessage-save.md) , en passant **null** dans le paramètre _pMessage_ et **la valeur true** dans le paramètre _fSameAsLoad_ . 
    
2. Il appelle la méthode **IMAPIViewContext::ActivateNext** , en passant l’indicateur VCDIR_DELETE dans le paramètre _ulDir_ . 
    
3. Si l’appel **ActivateNext** échoue, elle renvoie. Si **ActivateNext** renvoie S_FALSE, il appelle la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Il supprime ou déplace le message.
    
Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

