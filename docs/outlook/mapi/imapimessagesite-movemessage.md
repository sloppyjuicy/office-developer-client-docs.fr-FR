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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321364"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déplace le message actif vers un dossier.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Paramètres

 _pFolderDestination_
  
> dans Pointeur vers le dossier dans lequel le message doit être déplacé.
    
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

Les objets de formulaire appellent la méthode **IMAPIMessageSite:: MoveMessage** pour déplacer le message actif vers un nouveau dossier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L'implémentation d'une visionneuse de formulaires **MoveMessage** doit appeler la méthode [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md) , en transmettant l'indicateur VCDIR_MOVE, avant de placer le message dans un nouveau dossier. Pour obtenir la structure **Rect** utilisée par la fenêtre d'un formulaire, appelez la fonction [GetWindowRect](https://msdn.microsoft.com/library/ms633519) de Windows. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Suite au retour de **MoveMessage**, les formulaires doivent vérifier l'existence d'un message en cours, puis le faire disparaître s'il n'en existe pas. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: MoveMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

