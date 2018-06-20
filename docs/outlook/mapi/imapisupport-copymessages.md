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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 64b2c147acb02b6c29cf080076b6fe2e3eefb717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783969"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**S’applique à**: Outlook 
  
Copie ou déplace les messages d’un dossier dans un autre dossier.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier qui contient les messages à déplacer ou copier.
    
 _lpSrcFolder_
  
> [in] Pointeur vers le dossier qui contient les messages à déplacer ou copier.
    
 _lpMsgList_
  
> [in] Pointeur vers un tableau d’identificateurs d’entrée qui identifient les messages à déplacer ou copier. 
    
 _lpDestInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination pour les messages copiés ou déplacées.
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier de destination pour les messages copiés ou déplacées. Ce dossier doit être ouvert.
    
 _ulUIParam_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la manière dont l’opération de copie ou de déplacement est effectuée. Les indicateurs suivants peuvent être définis :
    
MESSAGE_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
MESSAGE_MOVE 
  
> Les messages doivent être déplacés, au lieu de copier. Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération de copie ou de déplacement a réussi.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::CopyMessages** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de magasins de message peuvent appeler **IMAPISupport::CopyMessages** dans leur implémentation [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pour copier ou déplacer un ou plusieurs messages d’un dossier à un autre. Dans le cadre de l’appel **IMAPISupport::CopyMessages** , le fournisseur de banque de messages permettre spécifier que MAPI doit afficher un indicateur de progression. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

