---
title: IMAPIFolderCreateFolder
description: IMAPIFolderCreateFolder crée un sous-dossier. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
ms.openlocfilehash: 308cfec97f5df8cb8178735646e38ac123a08b13
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818172"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un sous-dossier.
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a>Paramètres

 _ulFolderType_
  
> [in] Type de dossier à créer. Les indicateurs suivants peuvent être définis :
    
FOLDER_GENERIC 
  
> Un dossier générique doit être créé.
    
FOLDER_SEARCH 
  
> Un dossier de résultats de recherche doit être créé.
    
 _lpszFolderName_
  
> [in] Pointeur vers une chaîne qui contient le nom du nouveau dossier. Ce nom est la base de la propriété **PR_DISPLAY_NAME** du nouveau dossier ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
 _lpszFolderComment_
  
> [in] Pointeur vers une chaîne qui contient un commentaire associé au nouveau dossier. Cette chaîne devient la valeur de la propriété **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) du nouveau dossier. Si null est passé, le dossier n’a aucun commentaire initial.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau dossier. Si la valeur NULL est passée, le fournisseur du magasin de messages retourne l’interface de dossier standard [, IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent passer null. D’autres appelants peuvent définir le paramètre  _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont le dossier est créé. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **CreateFolder** de retourner correctement, éventuellement avant que le nouveau dossier soit entièrement disponible pour le client appelant. Si le nouveau dossier n’est pas disponible, l’appel suivant peut provoquer une erreur. 
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, le nom du dossier est au format ANSI.
    
OPEN_IF_EXISTS 
  
> Permet à la méthode de réussir même si le dossier nommé dans le paramètre _lpszFolderName_ existe déjà en ouvrant le dossier existant portant ce nom. Notez que les fournisseurs de magasins de messages qui autorisent les dossiers frères à avoir le même nom peuvent ne pas ouvrir un dossier existant s’il en existe plusieurs avec le nom fourni. 
    
 _lppFolder_
  
> [out] Pointeur vers un pointeur vers le dossier nouvellement créé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau dossier a été créé ou ouvert avec succès, si l’indicateur OPEN_IF_EXISTS est défini.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_COLLISION 
  
> Un dossier dont le nom est donné dans le paramètre _lpszFolderName_ existe déjà. Les noms de dossiers doivent être uniques. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CreateFolder** crée un sous-dossier dans le dossier actif et affecte un identificateur d’entrée au nouveau dossier. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **CreateFolder** est retourné, sachez que l’identificateur d’entrée du nouveau dossier peut ne pas être disponible. Certains fournisseurs de magasins de messages ne rendent les identificateurs d’entrée disponibles qu’après avoir appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du nouveau dossier pour l’enregistrer définitivement. Cela est particulièrement vrai si vous avez défini l’indicateur MAPI_DEFERRED_ERRORS. 
  
Sachez que certains fournisseurs de magasins de messages pointent toujours le paramètre  _lppFolder_ vers l’interface standard du dossier, quelle que soit la valeur que vous transmettez pour le paramètre  _lpInterface_ . Étant donné que le pointeur d’interface retourné peut ne pas être du type attendu, appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du nouveau dossier pour récupérer la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si nécessaire, cassez le pointeur vers un type plus approprié avant d’effectuer d’autres appels.
  
La plupart des fournisseurs de magasins de messages exigent que le nom du nouveau dossier soit unique en ce qui concerne les noms de ses dossiers frères. Être en mesure de gérer la valeur d’erreur MAPI_E_COLLISION, qui est retournée si cette règle n’est pas suivie. 
  
Pour déterminer l’identificateur d’entrée du dossier nouvellement créé, appelez la méthode **IMAPIProp::GetProps** du nouveau dossier pour récupérer sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI utilise la méthode **CMsgStoreDlg::OnCreateSubFolder** pour créer des dossiers dans MFCMAPI. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

