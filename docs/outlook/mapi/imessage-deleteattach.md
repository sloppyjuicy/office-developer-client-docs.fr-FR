---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592513"
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
  
> [in] Numéro d’index de la pièce jointe à supprimer. Il s’agit de la valeur de propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou de windows, que cette méthode affiche. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur ATTACH_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur ATTACH_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’affichage de l’interface utilisateur. Vous pouvez définir l’indicateur suivant :
    
ATTACH_DIALOG 
  
> Demande l’affichage d’un indicateur de progression de l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La pièce jointe a été supprimée.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::DeleteAttach** supprime une pièce jointe à partir d’un message. 
  
Une pièce jointe supprimée n’est pas définitivement supprimée jusqu'à ce que la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message a été appelée. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Avant d’appeler **DeleteAttach**, appelez la méthode **IUnknown::Release** pour la pièce jointe et chacun de ses flux. 
  
Étant donné que la suppression d’une pièce jointe peut être un processus long, **DeleteAttach** fournit le mécanisme qui affiche un indicateur de progression. Vous pouvez demander l’affichage d’un indicateur de progression en passant un pointeur vers votre [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implémentation ou NULL si vous ne disposez pas d’une implémentation. Vous devez également spécifier un handle de fenêtre dans le paramètre _ulUIParam_ et l’indicateur ATTACH_DIALOG dans le paramètre _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMessage::DeleteAttach** pour supprimer la pièce jointe sélectionnée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

