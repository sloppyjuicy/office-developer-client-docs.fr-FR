---
title: IMAPISupportCopyFolder
description: IMAPISupportCopyFolder copie ou déplace un dossier de son dossier parent actuel vers un autre dossier parent.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
ms.openlocfilehash: a48a9c4d3b5c994c5370f020e19f8e1949ff4421
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827897"
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par  _lpEntryID_.
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier à copier ou à déplacer. 
    
 _lpInterface_
  
> [in] Réservé; doit être NULL.
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier qui doit recevoir le dossier à copier ou à déplacer.
    
 _lpszNewFolderName_
  
> [in] Pointeur vers le nom du dossier copié ou déplacé ; sinon, NULL, qui indique que le dossier copié ou déplacé doit avoir le même nom que le dossier source (dossier pointé par  _lpEntryID_).
    
 _ulUIParam_
  
> [in] Handle de la fenêtre pour la boîte de dialogue indicateur de progression et les fenêtres associées. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est effectuée. Les indicateurs suivants peuvent être définis :
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers du dossier doivent être copiés ou déplacés. Lorsque COPY_SUBFOLDERS n’est pas défini pour une opération de copie, seul le dossier identifié par  _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut, que l’indicateur soit défini ou non. 
    
FOLDER_DIALOG 
  
> Demande l’affichage d’un indicateur de progression.
    
FOLDER_MOVE 
  
> Le dossier doit être déplacé au lieu d’être copié. Si FOLDER_MOVE n’est pas défini, le dossier est copié.
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été correctement copié ou déplacé.
    
MAPI_E_COLLISION 
  
> Le nom du dossier déplacé ou copié est le même que celui d’un sous-dossier dans le dossier de destination. Le fournisseur du magasin de messages exige que les noms de dossiers soient uniques. L’opération s’arrête sans se terminer.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été copiées avec succès. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::CopyFolder** est implémentée pour les objets de support du fournisseur du magasin de messages. Les fournisseurs de magasins de messages peuvent appeler **IMAPISupport::CopyFolder** dans leur implémentation [d’IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) pour copier ou déplacer un dossier unique d’un dossier parent vers un autre. 
  
 **IMAPISupport::CopyFolder** ajoute le dossier copié ou déplacé en tant que sous-dossier du dossier de destination. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **IMAPISupport::CopyFolder** permet de renommer et de déplacer simultanément des dossiers, ainsi que la copie ou le déplacement de sous-dossiers du dossier affecté. Pour copier ou déplacer tous les sous-dossiers imbriqués dans le dossier copié ou déplacé, transmettez l’indicateur COPY_SUBFOLDERS dans  _ulFlags_. 
  
Attendez-vous aux valeurs de retour suivantes dans les conditions suivantes :
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**CopyFolder** a correctement copié ou déplacé le dossier et tous ses sous-dossiers, le cas échéant. |S_OK  <br/> |
|**CopyFolder** n’a pas pu copier ou déplacer tous les dossiers. |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** n’a pas pu se terminer. |Toute valeur d’erreur  <br/> |
   
Si **CopyFolder** retourne une valeur d’erreur, ne procédez pas en partant du principe qu’aucun travail n’a été effectué. Un ou plusieurs dossiers auraient pu être copiés ou déplacés avant que **CopyFolder** n’ait rencontré l’échec. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

