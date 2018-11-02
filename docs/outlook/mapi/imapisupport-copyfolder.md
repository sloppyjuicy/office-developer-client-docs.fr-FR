---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ffbf74496d4b61357a0fb473b82deedf39ee576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570673"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace un dossier à partir de son dossier parent en cours vers un autre dossier parent.
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

 _lpSrcInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier parent du dossier à déplacer ou copier.
    
 _lpSrcFolder_
  
> [in] Pointeur vers le dossier parent du dossier à déplacer ou copier. 
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée désigné par _lpEntryID_.
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier à déplacer ou copier. 
    
 _lpInterface_
  
> [in] Réservé ; doit être NULL.
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier qui doit recevoir le dossier pour déplacer ou copier.
    
 _lpszNewFolderName_
  
> [in] Un pointeur vers le nom du dossier copié ou déplacé. dans le cas contraire, NULL, qui indique que le dossier copié ou déplacé doit avoir le même nom que le dossier source (le dossier vers lequel pointe _lpEntryID_).
    
 _ulUIParam_
  
> [in] Handle de la fenêtre de la boîte de dialogue de progression de l’indicateur et les fenêtres associées. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la manière dont l’opération de copie ou de déplacement est effectuée. Les indicateurs suivants peuvent être définis :
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers du dossier doivent être copiés ou déplacés. Lorsque COPY_SUBFOLDERS n’est pas définie pour une opération de copie, seul le dossier identifié par _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut que si l’indicateur est défini. 
    
FOLDER_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
FOLDER_MOVE 
  
> Le dossier doit être déplacé au lieu de copier. Si FOLDER_MOVE n’est pas défini, le dossier est copié.
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été copié ou déplacé.
    
MAPI_E_COLLISION 
  
> Le nom du dossier en cours de déplacer ou copier est la même que celle d’un sous-dossier dans le dossier de destination. Le fournisseur de banque de messages requiert que les noms de dossiers être uniques. L’opération s’arrête sans terminer.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais pas toutes les entrées ont été correctement copiées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::CopyFolder** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de magasins de message peuvent appeler **IMAPISupport::CopyFolder** dans leur implémentation [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) pour copier ou déplacer un seul dossier à partir du dossier parent d’un à l’autre. 
  
 **IMAPISupport::CopyFolder** ajoute le dossier copié ou déplacé comme un sous-dossier du dossier de destination. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **IMAPISupport::CopyFolder** permet de changement de nom et le déplacement de dossiers et la copie ou le déplacement de sous-dossiers du dossier concerné simultanées. Pour copier ou déplacer tous les sous-dossiers imbriqués dans le dossier copié ou déplacé, passez l’indicateur COPY_SUBFOLDERS _ulFlags_. 
  
Tirer que suivantes retournent des valeurs dans les conditions suivantes :
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder** correctement copié ou déplacé le dossier et tous ses sous-dossiers, le cas échéant.  <br/> |S_OK  <br/> |
|**CopyFolder** n’a pas pu copier ou déplacer tous les dossiers.  <br/> |MAPI_W_PARTIAL_COMPLETION SE PRODUIT  <br/> |
|**CopyFolder** n’a pas pu terminer.  <br/> |Une valeur d’erreur  <br/> |
   
Si **CopyFolder** renvoie une valeur d’erreur, ne poursuivez pas sur l’hypothèse où aucun travail a été effectuée. Un ou plusieurs dossiers peuvent copiés ou déplacés avant **CopyFolder** échec. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

