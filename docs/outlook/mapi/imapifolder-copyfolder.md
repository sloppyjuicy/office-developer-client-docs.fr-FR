---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5c4ddba0719056966021b73caf0d0bdbdb3364ab
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462275"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace un sous-folder.
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du sous-folder à copier ou déplacer.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier vers qui pointe le paramètre  _lpDestFolder_ . Si la valeur NULL est passé, le fournisseur de services retourne l’interface de dossier standard [, IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les valeurs  _valides pour lpInterface_ sont IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier ouvert pour recevoir le sous-dossier copié ou déplacé.
    
 _lpszNewFolderName_
  
> [in] Pointeur vers le nom du dossier copié ou déplacé dans sa nouvelle destination. Si  _lpszNewFolderName_ est définie sur NULL, le nom du sous-dossier source est utilisé pour le nom du dossier de destination. 
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression. Le  _paramètre ulUIParam_ est ignoré, sauf si l’FOLDER_DIALOG dans le _paramètre ulFlags_ est définie. 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress_, le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’FOLDER_DIALOG est définie dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définies :
    
COPY_SUBFOLDERS 
  
> Tous les sous-sous-foldeurs à copier doivent également être copiés. Lorsque COPY_SUBFOLDERS n’est pas défini pour une opération de copie, seul le sous-foldeur identifié par  _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est le comportement par défaut, que l’indicateur soit ou non définie. 
    
FOLDER_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
FOLDER_MOVE 
  
> Le sous-folder doit être déplacé au lieu d’être copié. Si FOLDER_MOVE n’est pas définie, le sous-foldeur est copié.
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur de la boutique de messages que s’il implémente **CopyFolder** en appelant la méthode [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) de l’objet de support, **CopyFolder** doit renvoyer immédiatement MAPI_E_DECLINE_COPY. 
    
MAPI_UNICODE 
  
> Le nom du dossier de destination est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier spécifié a été correctement copié ou déplacé.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et le fournisseur de banque de messages ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de banque de messages prend uniquement en charge Unicode.
    
MAPI_E_COLLISION 
  
> Le nom du dossier déplacé ou copié est identique à celui d’un sous-dossier dans le dossier de destination. Le fournisseur de la boutique de messages requiert des noms de dossiers uniques.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode objet de support, et l’appelant a passé l’MAPI_DECLINE_OK’indicateur.
    
MAPI_E_FOLDER_CYCLE 
  
> Le dossier source contient directement ou indirectement le dossier de destination. Des travaux importants ont peut-être été effectués avant la découverte de cette condition, de sorte que le dossier source et le dossier de destination peuvent être partiellement modifiés. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été correctement copiées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED’avertissement** . Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::CopyFolder** copie ou déplace un sous-foldeur d’un emplacement à un autre. Le sous-dossier en cours de copie ou de déplacé est ajouté au dossier de destination en tant que sous-dossier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l’opération de copie ou de déplacement implique plusieurs dossiers, comme indiqué par la définition de l’indicateur COPY_SUBFOLDERS, effectuez l’opération aussi complètement que possible pour chaque dossier. Parfois, l’un des dossiers à déplacer ou à copier n’existe pas ou a déjà été déplacé ou copié ailleurs. N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.
  
Essayez de conserver tous les identificateurs d’entrée de message dans les messages copiés. Vous devez également essayer de conserver les identificateurs d’entrée, mais cela n’est pas obligatoire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder a** correctement copié ou déplacé chaque message et sous-folder.  <br/> |S_OK  <br/> |
|**CopyFolder n’a** pas pu copier ou déplacer correctement chaque message et sous-folder.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder n’a** pas pu se terminer.  <br/> |Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **CopyFolder ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué. **CopyFolder a** peut-être pu copier ou déplacer un ou plusieurs des messages et sous-foldeurs avant de rencontrer l’erreur. 
  
Si un identificateur d’entrée pour un dossier qui n’existe pas est transmis dans  _lpEntryID_, **CopyFolder** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la magasin de messages. 
  
Selon le fournisseur de la boutique de messages, l’identificateur d’entrée du message d’origine peut ou non être conservé dans le message copié. Vous devez conserver les identificateurs d’entrée chaque fois que possible, mais ce n’est pas obligatoire. Vous pouvez généralement dépendre des scénarios suivants :
  
- Lorsque vous déplacez un dossier entre deux types différents de magasins de messages, il est garanti que l’identificateur d’entrée change.
    
- Lorsque vous déplacez un dossier entre deux magasins de messages du même type, l’identificateur d’entrée change presque toujours.
    
- Lorsque vous déplacez un dossier vers un autre emplacement dans la même magasin de messages, l’identificateur d’entrée peut changer ou non, selon le fournisseur de la boutique de messages.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI utilise la **méthode IMAPIFolder::CopyFolder** pour copier des dossiers d’un emplacement à un autre. MFCMAPI se souvenir du dossier source pendant l’opération de copie et effectue en fait la copie pendant l’opération de coller.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

