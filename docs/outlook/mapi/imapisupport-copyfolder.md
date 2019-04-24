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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341026"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace un dossier à partir de son dossier parent actuel vers un autre dossier parent.
  
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
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier parent du dossier à copier ou déplacer.
    
 _lpSrcFolder_
  
> dans Pointeur vers le dossier parent du dossier à copier ou déplacer. 
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par _lpEntryID_.
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du dossier à copier ou déplacer. 
    
 _lpInterface_
  
> dans MSR doit être NULL.
    
 _lpDestFolder_
  
> dans Pointeur vers le dossier qui doit recevoir le dossier à copier ou déplacer.
    
 _lpszNewFolderName_
  
> dans Pointeur vers le nom du dossier copié ou déplacé; Sinon, NULL, ce qui indique que le dossier copié ou déplacé doit avoir le même nom que le dossier source (le dossier pointé par _lpEntryID_).
    
 _ulUIParam_
  
> dans Handle de la fenêtre de la boîte de dialogue indicateur de progression et fenêtres associées. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
COPY_SUBFOLDERS 
  
> Tous les sous-dossiers du dossier doivent être copiés ou déplacés. Lorsque COPY_SUBFOLDERS n'est pas défini pour une opération de copie, seul le dossier identifié par _lpEntryID_ est copié. Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut, que l'indicateur soit défini ou non. 
    
FOLDER_DIALOG 
  
> Demande l'affichage d'un indicateur de progression.
    
FOLDER_MOVE 
  
> Le dossier doit être déplacé au lieu d'être copié. Si FOLDER_MOVE n'est pas défini, le dossier est copié.
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du dossier est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été correctement copié ou déplacé.
    
MAPI_E_COLLISION 
  
> Le nom du dossier déplacé ou copié est le même que celui d'un sous-dossier dans le dossier de destination. Le fournisseur de banque de messages exige que les noms de dossier soient uniques. L'opération s'arrête sans terminer.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'appel a réussi, mais toutes les entrées n'ont pas été correctement copiées. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: CopyFolder** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages peuvent appeler **IMAPISupport: CopyFolder** dans leur implémentation de [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) pour copier ou déplacer un dossier unique d'un dossier parent vers un autre. 
  
 **IMAPISupport:: CopyFolder** ajoute le dossier copié ou déplacé en tant que sous-dossier du dossier de destination. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **IMAPISupport:: CopyFolder** permet le changement de nom et le transfert simultanés de dossiers, ainsi que la copie ou le transfert des sous-dossiers du dossier affecté. Pour copier ou déplacer tous les sous-dossiers imbriqués dans le dossier copié ou déplacé, transmettez l'indicateur COPY_SUBFOLDERS dans _ulFlags_. 
  
Prévoyez les valeurs de retour suivantes dans les conditions suivantes:
  
|**Condition**|**Valeur renvoyée**|
|:-----|:-----|
|**CopyFolder** a copié ou déplacé le dossier et tous ses sous-dossiers, le cas échéant.  <br/> |S_OK  <br/> |
|**CopyFolder** n'a pas pu copier ou déplacer tous les dossiers.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** n'a pas pu être terminé.  <br/> |Toute valeur d'erreur  <br/> |
   
Si **CopyFolder** renvoie une valeur d'erreur, ne continuez pas en supposant qu'aucun travail n'a été effectué. Un ou plusieurs dossiers ont pu être copiés ou déplacés avant que **CopyFolder** ait rencontré l'échec. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

