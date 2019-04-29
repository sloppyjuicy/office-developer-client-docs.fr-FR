---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425658"
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du sous-dossier à copier ou déplacer.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier vers lequel pointe le paramètre _lpDestFolder_ . Si vous passez la valeur NULL, le fournisseur de services renvoie l'interface de dossier standard, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Les valeurs valides pour _lpInterface_ sont IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> dans Pointeur vers le dossier ouvert qui reçoit le sous-dossier copié ou déplacé.
    
 _lpszNewFolderName_
  
> dans Pointeur vers le nom du dossier copié ou déplacé dans sa nouvelle destination. Si _lpszNewFolderName_ est défini sur null, le nom du sous-dossier source est utilisé pour le nom du dossier de destination. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur FOLDER_DIALOG dans le paramètre _ulFlags_ est défini. 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers du sous-dossier à copier doivent également être copiés. Lorsque COPY_SUBFOLDERS n'est pas défini pour une opération de copie, seul le sous-dossier identifié par _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut, que l'indicateur soit défini ou non. 
    
FOLDER_DIALOG 
  
> Demande l'affichage d'un indicateur de progression.
    
FOLDER_MOVE 
  
> Le sous-dossier doit être déplacé au lieu d'être copié. Si FOLDER_MOVE n'est pas défini, le sous-dossier est copié.
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur de banque de messages que s'il implémente **CopyFolder** en appelant la méthode IMAPISupport de l'objet de prise en charge [::D ocopyto](imapisupport-docopyto.md) ou [IMAPISupport::D méthode ocopyprops](imapisupport-docopyprops.md) , **CopyFolder** doit renvoyer immédiatement MAPI_E_ DECLINE_COPY. 
    
MAPI_UNICODE 
  
> Le nom du dossier de destination est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier spécifié a été correctement copié ou déplacé.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et le fournisseur de banque de messages ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de banque de messages prend en charge uniquement Unicode.
    
MAPI_E_COLLISION 
  
> Le nom du dossier déplacé ou copié est le même que celui d'un sous-dossier dans le dossier de destination. Le fournisseur de banque de messages requiert des noms de dossier uniques.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode d'objet de prise en charge, et l'appelant a passé l'indicateur MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> Le dossier source contient directement ou indirectement le dossier de destination. Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que le dossier source et de destination peut être partiellement modifié. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'appel a réussi, mais toutes les entrées n'ont pas été correctement copiées. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: CopyFolder** copie ou déplace un sous-dossier d'un emplacement à un autre. Le sous-dossier copié ou déplacé est ajouté au dossier de destination sous la forme d'un sous-dossier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l'opération de copie ou de déplacement implique plusieurs dossiers, comme indiqué par la définition de l'indicateur COPY_SUBFOLDERS, effectuez l'opération aussi complètement que possible pour chaque dossier. Parfois, l'un des dossiers à déplacer ou à copier n'existe pas ou a déjà été déplacé ou copié ailleurs. N'arrêtez pas l'opération prématurément à moins qu'une défaillance ne se produise au-delà de votre contrôle, telle qu'une mémoire insuffisante, un manque d'espace disque ou une corruption de la Banque de messages.
  
Essayez de conserver tous les identificateurs d'entrée de message dans les messages copiés. Vous devez également essayer de conserver les identificateurs d'entrée, mais cela n'est pas obligatoire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder** a copié ou déplacé tous les messages et sous-dossiers.  <br/> |S_OK  <br/> |
|**CopyFolder** n'a pas pu copier ou déplacer tous les messages et sous-dossiers.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** n'a pas pu être terminé.  <br/> |Toute valeur d'erreur à l'exception de MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **CopyFolder** ne parvient pas à se terminer, ne partez pas du principe qu'aucun travail n'a été effectué. **CopyFolder** a pu copier ou déplacer un ou plusieurs messages et sous-dossiers avant de rencontrer l'erreur. 
  
Si un identificateur d'entrée pour un dossier qui n'existe pas est transmis dans _lpEntryID_, **CopyFolder** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l'implémentation de la Banque de messages. 
  
Selon le fournisseur de banque de messages, l'identificateur d'entrée du message d'origine peut ou non être conservé dans le message copié. Vous devez conserver les identificateurs d'entrée autant que possible, mais cela n'est pas obligatoire. Vous pouvez généralement compter sur les scénarios suivants:
  
- Lorsque vous déplacez un dossier entre deux types différents de banques de messages, l'identificateur de l'entrée est garanti.
    
- Lorsque vous déplacez un dossier entre deux banques de messages du même type, l'identificateur de l'entrée est presque toujours modifié.
    
- Lorsque vous déplacez un dossier vers un autre emplacement dans le même magasin de messages, l'identificateur de l'entrée peut être modifié ou non, selon le fournisseur de banque de messages.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnPasteFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFolder:: CopyFolder** pour copier les dossiers d'un emplacement à un autre. MFCMAPI mémorise le dossier source pendant l'opération de copie et effectue la copie lors de l'opération de collage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

