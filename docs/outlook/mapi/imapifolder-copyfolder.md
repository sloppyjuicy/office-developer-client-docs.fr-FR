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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5961e7a2118a46bdc9c0e66138363976ae2f7154
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783723"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**S’applique à**: Outlook 
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du sous-dossier pour copier ou déplacer.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier vers lequel pointe le paramètre _lpDestFolder_ . Passage de NULL entraîne le fournisseur de services renvoyer l’interface dossier standard, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les valeurs valides pour _lpInterface_ sont IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier ouvert pour recevoir le sous-dossier copié ou déplacé.
    
 _lpszNewFolderName_
  
> [in] Pointeur vers le nom du dossier copié ou déplacé dans son nouvel emplacement. Si _lpszNewFolderName_ est défini sur NULL, le nom du sous-dossier source est utilisé pour le nom du dossier de destination. 
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur FOLDER_DIALOG dans le paramètre _ulFlags_ est défini. 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers dans le sous-dossier à copier doivent également être copiés. Lorsque COPY_SUBFOLDERS n’est pas définie pour une opération de copie, uniquement dans le sous-dossier identifié par _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut que si l’indicateur est défini. 
    
FOLDER_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
FOLDER_MOVE 
  
> Le sous-dossier doit être déplacé au lieu de copier. Si FOLDER_MOVE n’est pas défini, le sous-dossier est copié.
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur de banque de messages que s’il implémente **CopyFolder** en appelant la méthode [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) de l’objet de la prise en charge, **CopyFolder** doit retourner à la place immédiatement MAPI_E_ DECLINE_COPY. 
    
MAPI_UNICODE 
  
> Le nom du dossier de destination est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le dossier spécifié a été copié ou déplacé.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de banque de messages ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et prend en charge le fournisseur de banque de message Unicode uniquement.
    
MAPI_E_COLLISION 
  
> Le nom du dossier en cours de déplacer ou copier est la même que celle d’un sous-dossier dans le dossier de destination. Le fournisseur de banque de messages exige que les noms de dossier unique.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode de prise en charge de l’objet et l’appelant a passé l’indicateur MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> Le dossier source, directement ou indirectement contient le dossier de destination. Travail significatifs a peut-être été effectué avant cette condition a été détectée, le dossier source et de destination peut être modifié partiellement. 
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais pas toutes les entrées ont été correctement copiées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CopyFolder** copie ou déplace un sous-dossier d’un emplacement vers un autre. Le sous-dossier copiées ou déplacées est ajouté au dossier de destination, comme un sous-dossier. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Lorsque l’opération de copie ou de déplacement implique plusieurs dossiers, comme indiqué par l’indicateur COPY_SUBFOLDERS, effectuez l’opération complètement que possible pour chaque dossier. Parfois, un des dossiers d’être déplacé ou copié n’existe pas ou a déjà été déplacé ou copié ailleurs. N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.
  
Essayez de conserver tous les identificateurs d’entrée de message dans les messages copiés. Vous devriez également conserver les identificateurs d’entrée, mais il n’est pas nécessaire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Prévoyez ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder** a été copié ou déplacé tous les messages et sous-dossier.  <br/> |S_OK  <br/> |
|**CopyFolder** n’a pas pu copier ou déplacer tous les messages et sous-dossier.  <br/> |MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** n’a pas pu terminer.  <br/> |Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **CopyFolder** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée. **CopyFolder** peut-être en mesure de copier ou déplacer une ou plusieurs des messages et les sous-dossiers avant de rencontrer l’erreur. 
  
Si un identificateur pour un dossier qui n’existe pas d’entrée est passé dans _lpEntryID_, **CopyFolder** renvoie MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la banque de messages. 
  
Selon le fournisseur de banque de message, l’identificateur d’entrée du message d’origine peut-être ou ne peut pas être conservé dans le message copié. Vous devez conserver les identificateurs d’entrée la mesure du possible, mais il n’est pas une condition requise. Vous pouvez généralement dépendent les scénarios suivants :
  
- Lorsque vous déplacez un dossier entre les deux types de banques de messages, l’identificateur d’entrée est garanti à modifier.
    
- Lorsque vous déplacez un dossier entre deux bases de messages du même type, l’identificateur d’entrée change presque toujours.
    
- Lorsque vous déplacez un dossier à un autre emplacement dans le même magasin de message, l’identificateur d’entrée peut ou ne peut-être pas modifier, selon le message le fournisseur de magasins.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::CopyFolder** pour copier des dossiers d’un emplacement vers un autre. MFCMAPI mémorise le dossier source pendant l’opération de copie et effectue la copie pendant l’opération de collage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

