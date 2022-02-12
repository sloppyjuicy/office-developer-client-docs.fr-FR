---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fd936d0c5cf2d35a11bb8c701451238ffcde5182
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773431"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déplace le message actuel vers un dossier.
  
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
  
> [in] Pointeur vers un objet de contexte d’affichage.
    
 _prcPosRect_
  
> [in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la taille et la position de la fenêtre du formulaire actuel. Le formulaire suivant affiché utilise également ce rectangle de fenêtre. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas prise en charge par ce site de message.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIMessageSite::MoveMessage** pour déplacer le message actuel vers un nouveau dossier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L’implémentation de **MoveMessage** d’une visionneuse de formulaire doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , en passant l’indicateur VCDIR_MOVE, avant de déplacer réellement le message vers un nouveau dossier. Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez Windows [fonction GetWindowRect](https://msdn.microsoft.com/library/ms633519). 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [INTERFACES DE FORMULAIRE MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Après le renvoi de **MoveMessage, les formulaires** doivent vérifier la recherche d’un message actuel, puis se fermer s’il n’en existe aucun. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Non implémenté. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

