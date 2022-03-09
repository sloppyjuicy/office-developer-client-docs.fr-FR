---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
ms.openlocfilehash: d932b02abed11b5cb9667db00c822b8a78249ac6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370847"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace des messages d’un dossier vers un autre dossier.
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpSrcInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier qui contient les messages à copier ou à déplacer.
    
 _lpSrcFolder_
  
> [in] Pointeur vers le dossier qui contient les messages à copier ou à déplacer.
    
 _lpMsgList_
  
> [in] Pointeur vers un tableau d’identificateurs d’entrée qui identifient les messages à copier ou à déplacer. 
    
 _lpDestInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination des messages copiés ou déplacés.
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier de destination pour les messages copiés ou déplacés. Ce dossier doit être ouvert.
    
 _ulUIParam_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress_, le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans  _ulFlags_.
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress_, le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est accomplie. Les indicateurs suivants peuvent être définies :
    
MESSAGE_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
MESSAGE_MOVE 
  
> Les messages doivent être déplacés au lieu d’être copiés. Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de copie ou de déplacement a réussi.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le **bouton Annuler dans** une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::CopyMessages** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages peuvent appeler **IMAPISupport::CopyMessages** dans leur implémentation [d’IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pour copier ou déplacer un ou plusieurs messages d’un dossier vers un autre. Dans le cadre de l’appel **IMAPISupport::CopyMessages** , le fournisseur de magasin de messages peut spécifier que MAPI doit afficher un indicateur de progression. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

