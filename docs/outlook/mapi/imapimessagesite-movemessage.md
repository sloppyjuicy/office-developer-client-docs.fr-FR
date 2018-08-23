---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e12ce442540930d9fa366ced073afc4828a01244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576112"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Déplace le message en cours dans un dossier.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Paramètres

 _pFolderDestination_
  
> [in] Pointeur vers le dossier dans lequel le message doit être déplacé.
    
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

Objets de formulaire appeler la méthode **IMAPIMessageSite::MoveMessage** pour déplacer le message en cours vers un nouveau dossier. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Implémentation de l’utilisateur du formulaire de **MoveMessage** doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , en passant l’indicateur VCDIR_MOVE, avant de déplacer réellement le message vers un nouveau dossier. Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Notes aux appelants

Après le renvoi de **MoveMessage**, formulaires doivent vérifier pour un message en cours et se fermer puis si aucune n’existe. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaires MAPI](mapi-form-interfaces.md)

