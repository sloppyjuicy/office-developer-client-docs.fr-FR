---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416782"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime tous les messages et sous-dossiers d'un dossier sans supprimer le dossier lui-même.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le dossier est vidé. Les indicateurs suivants peuvent être définis:
    
DEL_ASSOCIATED 
  
> Supprime tous les sous-dossiers, y compris les sous-dossiers qui contiennent des messages avec du contenu associé. L'indicateur DEL_ASSOCIATED n'a de sens que pour le dossier de niveau supérieur sur lequel l'appel agit.
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris ceux qui sont supprimés de manière récupérable.
    
FOLDER_DIALOG 
  
> Affiche un indicateur de progression pendant l'exécution de l'opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été vidé.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'appel a réussi, mais le dossier n'a pas été complètement vidé. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: EmptyFolder** supprime tout le contenu d'un dossier sans supprimer le dossier lui-même. 
  
Lors d'un appel **EmptyFolder** , les messages soumis ne sont pas supprimés. 
  
Le contenu associé d'un dossier inclut les messages qui sont utilisés pour décrire les vues, les règles, les formulaires personnalisés et le stockage de solutions personnalisées, et peut également inclure des définitions de formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

N'appelez pas la méthode [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) pour les messages qui ont été envoyés dans le dossier. Les messages envoyés ne sont pas supprimés. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**EmptyFolder** a correctement vidé le dossier.  <br/> |S_OK  <br/> |
|**EmptyFolder** n'a pas pu complètement vider le dossier.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** n'a pas pu être exécuté.  <br/> |Toute valeur d'erreur  <br/> |
   
Lorsque **EmptyFolder** ne parvient pas à terminer, ne partez pas du principe qu'aucun travail n'a été effectué. **EmptyFolder** peut avoir pu supprimer une partie du contenu du dossier avant de rencontrer l'erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnEmptyFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFolder:: EmptyFolder** pour supprimer le contenu du dossier spécifié.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

