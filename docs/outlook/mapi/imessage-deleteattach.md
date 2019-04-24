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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351078"
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
  
> dans Numéro d'index de la pièce jointe à supprimer. Il s'agit de la valeur de la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.
    
 _ulUIParam_
  
> dans Handle vers la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur ATTACH_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur ATTACH_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'affichage d'une interface utilisateur. L'indicateur suivant peut être défini:
    
ATTACH_DIALOG 
  
> Demande l'affichage d'un indicateur de progression pendant l'exécution de l'opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La pièce jointe a été supprimée.
    
## <a name="remarks"></a>Remarques

La méthode **Eleteattach IMessage::D** supprime une pièce jointe dans un message. 
  
Une pièce jointe supprimée n'est pas définitivement supprimée tant que la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message n'a pas été appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Avant d'appeler **DeleteAttach**, appelez la méthode **IUnknown:: Release** pour la pièce jointe et chacun de ses flux. 
  
Étant donné que la suppression d'une pièce jointe peut être un processus long, **DeleteAttach** fournit un indicateur de progression. Vous pouvez demander l'affichage d'un indicateur de progression en passant un pointeur vers votre implémentation [méthode imapiprogress: IUnknown](imapiprogressiunknown.md) ou null si vous ne disposez pas d'une implémentation. Vous devez également spécifier un descripteur de fenêtre dans le paramètre _ulUIParam_ et l'indicateur ATTACH_DIALOG dans le paramètre _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp  <br/> |CAttachmentsDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMessage::D eleteattach** pour supprimer la pièce jointe sélectionnée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

