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
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420884"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace un dossier de son dossier parent actuel vers un autre dossier parent.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier parent du dossier à copier ou à déplacer.
    
 _lpSrcFolder_
  
> [in] Pointeur vers le dossier parent du dossier à copier ou à déplacer. 
    
 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _lpEntryID_.
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier à copier ou à déplacer. 
    
 _lpInterface_
  
> [in] Réservé ; doit être NULL.
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier qui doit recevoir le dossier à copier ou à déplacer.
    
 _lpszNewFolderName_
  
> [in] Pointeur vers le nom du dossier copié ou déplacé ; sinon, NULL, qui indique que le dossier copié ou déplacé doit avoir le même nom que le dossier source (le dossier pointé par  _lpEntryID_).
    
 _ulUIParam_
  
> [in] Handle de la fenêtre pour la boîte de dialogue indicateur de progression et les fenêtres associées. Le _paramètre ulUIParam_ est ignoré, sauf si l’FOLDER_DIALOG est définie dans _le paramètre ulFlags._ 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’FOLDER_DIALOG est définie dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est accomplie. Les indicateurs suivants peuvent être définies :
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers du dossier doivent être copiés ou déplacés. Lorsque COPY_SUBFOLDERS n’est pas défini pour une opération de copie, seul le dossier identifié par  _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est le comportement par défaut, que l’indicateur soit ou non définie. 
    
FOLDER_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
FOLDER_MOVE 
  
> Le dossier doit être déplacé au lieu d’être copié. Si FOLDER_MOVE n’est pas définie, le dossier est copié.
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été correctement copié ou déplacé.
    
MAPI_E_COLLISION 
  
> Le nom du dossier déplacé ou copié est identique à celui d’un sous-dossier dans le dossier de destination. Le fournisseur de la boutique de messages exige que les noms de dossier soient uniques. L’opération s’arrête sans se terminer.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été correctement copiées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::CopyFolder** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages peuvent appeler **IMAPISupport::CopyFolder** dans leur implémentation [d’IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) pour copier ou déplacer un dossier unique d’un dossier parent vers un autre. 
  
 **IMAPISupport::CopyFolder** ajoute le dossier copié ou déplacé en tant que sous-dossier du dossier de destination. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **IMAPISupport::CopyFolder** permet le changement de nom et le déplacement simultanés de dossiers, ainsi que la copie ou le déplacement de sous-dossiers du dossier concerné. Pour copier ou déplacer tous les sous-dossiers imbriqués dans le dossier copié ou déplacé, passez l’COPY_SUBFOLDERS dans  _ulFlags_. 
  
Attendez-vous à ce que les valeurs de retour suivantes se placent dans les conditions suivantes :
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder a** correctement copié ou déplacé le dossier et tous ses sous-dossiers, le cas échéant.  <br/> |S_OK  <br/> |
|**CopyFolder n’a** pas pu copier ou déplacer tous les dossiers.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder n’a** pas pu se terminer.  <br/> |Toute valeur d’erreur  <br/> |
   
Si **CopyFolder renvoie** une valeur d’erreur, ne continuez pas sur l’hypothèse qu’aucun travail n’a été effectué. Un ou plusieurs dossiers ont pu être copiés ou déplacés avant **que CopyFolder** ne soit mis en échec. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

