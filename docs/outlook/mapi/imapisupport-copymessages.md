---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405155"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace les messages d'un dossier vers un autre dossier.
  
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
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier qui contient les messages à copier ou déplacer.
    
 _lpSrcFolder_
  
> dans Pointeur vers le dossier qui contient les messages à copier ou déplacer.
    
 _lpMsgList_
  
> dans Pointeur vers un tableau d'identificateurs d'entrée qui identifient les messages à copier ou déplacer. 
    
 _lpDestInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier de destination pour les messages copiés ou déplacés.
    
 _lpDestFolder_
  
> dans Pointeur vers le dossier de destination pour les messages copiés ou déplacés. Ce dossier doit être ouvert.
    
 _ulUIParam_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
MESSAGE_DIALOG 
  
> Demande l'affichage d'un indicateur de progression.
    
MESSAGE_MOVE 
  
> Les messages doivent être déplacés au lieu d'être copiés. Si MESSAGE_MOVE n'est pas défini, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de copie ou de déplacement a réussi.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: CopyMessages** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages peuvent appeler **IMAPISupport:: CopyMessages** dans leur implémentation de [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) pour copier ou déplacer un ou plusieurs messages d'un dossier à un autre. Dans le cadre de l'appel **IMAPISupport:: CopyMessages** , le fournisseur de banque de messages peut spécifier que MAPI doit afficher un indicateur de progression. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

