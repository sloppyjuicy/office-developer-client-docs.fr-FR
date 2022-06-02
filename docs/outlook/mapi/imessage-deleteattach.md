---
title: IMessageDeleteAttach
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IMessageDeleteAttach, qui supprime une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
ms.openlocfilehash: d1f380f70b05d88cc9b3afaae05eb85f081e5e4c
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827757"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une pièce jointe.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulAttachmentNum_
  
> [in] Numéro d’index de la pièce jointe à supprimer. Il s’agit de la valeur de la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber) de](pidtagattachnumber-canonical-property.md) la pièce jointe.
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows this method displays. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur ATTACH_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur ATTACH_DIALOG est défini dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent l’affichage d’une interface utilisateur. L’indicateur suivant peut être défini :
    
ATTACH_DIALOG 
  
> Demande l’affichage d’un indicateur de progression à mesure que l’opération se poursuit.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La pièce jointe a été supprimée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::D eleteAttach** supprime une pièce jointe d’un message. 
  
Une pièce jointe supprimée n’est pas supprimée définitivement tant que la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message n’a pas été appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Avant d’appeler **DeleteAttach**, appelez la méthode **IUnknown::Release** pour la pièce jointe et chacun de ses flux. 
  
Étant donné que la suppression d’une pièce jointe peut être un processus long, **DeleteAttach** fournit le mécanisme qui affiche un indicateur de progression. Vous pouvez demander l’affichage d’un indicateur de progression en passant un pointeur vers votre implémentation [IMAPIProgress : IUnknown](imapiprogressiunknown.md) ou NULL si vous n’avez pas d’implémentation. Vous devez également spécifier un handle de fenêtre dans le paramètre _ulUIParam_ et l’indicateur ATTACH_DIALOG dans le paramètre _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMessage::D eleteAttach** pour supprimer la pièce jointe sélectionnée. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

