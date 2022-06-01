---
title: IMAPIFolderCopyFolder
description: IMAPIFolderCopyFolder copie ou déplace un sous-dossier. Cet article décrit ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 49e0e2ff4ab242ee26591e5e726150d06479daf8
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816191"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace un sous-dossier.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du sous-dossier à copier ou à déplacer.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier vers lequel pointe le paramètre  _lpDestFolder_ . La transmission de la valeur NULL entraîne le retour de l’interface de dossier standard [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les valeurs valides pour  _lpInterface_ incluent IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier ouvert pour recevoir le sous-dossier copié ou déplacé.
    
 _lpszNewFolderName_
  
> [in] Pointeur vers le nom du dossier copié ou déplacé dans sa nouvelle destination. Si  _lpszNewFolderName_ a la valeur NULL, le nom du sous-dossier source est utilisé pour le nom du dossier de destination. 
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur FOLDER_DIALOG dans le paramètre _ulFlags_ est défini. 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers du sous-dossier à copier doivent également être copiés. Lorsque COPY_SUBFOLDERS n’est pas défini pour une opération de copie, seul le sous-dossier identifié par  _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut, que l’indicateur soit défini ou non. 
    
FOLDER_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
FOLDER_MOVE 
  
> Le sous-dossier doit être déplacé au lieu d’être copié. Si FOLDER_MOVE n’est pas défini, le sous-dossier est copié.
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur du magasin de messages que s’il **implémente CopyFolder** en appelant la méthode [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) de son objet de support, **CopyFolder** doit retourner immédiatement MAPI_E_DECLINE_COPY. 
    
MAPI_UNICODE 
  
> Le nom du dossier de destination est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier spécifié a été correctement copié ou déplacé.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur du magasin de messages ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et le fournisseur de magasin de messages prend uniquement en charge Unicode.
    
MAPI_E_COLLISION 
  
> Le nom du dossier déplacé ou copié est le même que celui d’un sous-dossier dans le dossier de destination. Le fournisseur du magasin de messages requiert des noms de dossiers uniques.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode objet de support, et l’appelant a passé l’indicateur MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> Le dossier source contient directement ou indirectement le dossier de destination. Un travail important peut avoir été effectué avant la découverte de cette condition, de sorte que le dossier source et le dossier de destination peuvent être partiellement modifiés. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été copiées avec succès. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CopyFolder** copie ou déplace un sous-dossier d’un emplacement à un autre. Le sous-dossier copié ou déplacé est ajouté au dossier de destination en tant que sous-dossier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l’opération de copie ou de déplacement implique plusieurs dossiers, comme indiqué en définissant l’indicateur COPY_SUBFOLDERS, effectuez l’opération aussi complètement que possible pour chaque dossier. Parfois, l’un des dossiers à déplacer ou à copier n’existe pas ou a déjà été déplacé ou copié ailleurs. N’arrêtez pas l’opération prématurément, à moins qu’une défaillance ne soit hors de votre contrôle, comme un manque de mémoire, un manque d’espace disque ou une altération du magasin de messages.
  
Essayez de conserver tous les identificateurs d’entrée de message dans les messages copiés. Vous devez également essayer de conserver les identificateurs d’entrée, mais ce n’est pas obligatoire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder** a correctement copié ou déplacé chaque message et sous-dossier. |S_OK  <br/> |
|**CopyFolder** n’a pas pu copier ou déplacer correctement chaque message et sous-dossier. |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** n’a pas pu se terminer. |Toute valeur d’erreur sauf MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **CopyFolder** n’est pas en mesure de se terminer, ne partez pas du principe qu’aucun travail n’a été effectué. **CopyFolder** a peut-être pu copier ou déplacer un ou plusieurs messages et sous-dossiers avant de rencontrer l’erreur. 
  
Si un identificateur d’entrée pour un dossier qui n’existe pas est passé dans  _lpEntryID_, **CopyFolder** retourne MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation du magasin de messages. 
  
Selon le fournisseur du magasin de messages, l’identificateur d’entrée du message d’origine peut ou non être conservé dans le message copié. Vous devez conserver les identificateurs d’entrée dans la mesure du possible, mais ce n’est pas obligatoire. Vous pouvez généralement dépendre des scénarios suivants :
  
- Lorsque vous déplacez un dossier entre deux types différents de magasins de messages, l’identificateur d’entrée est garanti pour changer.
    
- Lorsque vous déplacez un dossier entre deux magasins de messages du même type, l’identificateur d’entrée change presque toujours.
    
- Lorsque vous déplacez un dossier vers un autre emplacement dans le même magasin de messages, l’identificateur d’entrée peut ou non changer, en fonction du fournisseur du magasin de messages.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::CopyFolder** pour copier des dossiers d’un emplacement à un autre. MFCMAPI mémorise le dossier source pendant l’opération de copie et effectue réellement la copie pendant l’opération de collage. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

