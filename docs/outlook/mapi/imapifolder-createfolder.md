---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 694f7ec5715a7348c9bd90c28d14f30d43d19974
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581782"
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
  
> [in] Le type du dossier à créer. Les indicateurs suivants peuvent être définis :
    
FOLDER_GENERIC 
  
> Un dossier générique doit être créé.
    
FOLDER_SEARCH 
  
> Un dossier de résultats de recherche doit être créé.
    
 _lpszFolderName_
  
> [in] Pointeur vers une chaîne qui contient le nom du nouveau dossier. Ce nom sert de propriété de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du nouveau dossier.
    
 _lpszFolderComment_
  
> [in] Pointeur vers une chaîne qui contient un commentaire associé au nouveau dossier. Cette chaîne devient la valeur de propriété de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) du nouveau dossier. Si NULL est indiqué, le dossier n’a aucun commentaire initiale.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau dossier. Passage de NULL entraîne le fournisseur de banque de messages renvoyer l’interface dossier standard, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent passer la valeur NULL. Autres appelants peuvent de définir le paramètre _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est créé. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet de **CreateFolder** renvoyer avec succès, éventuellement avant le nouveau dossier est entièrement disponible au client appelant. Si le nouveau dossier n’est pas disponible, vous appelez suivante lui peut provoquer une erreur. 
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.
    
OPEN_IF_EXISTS 
  
> Permet à la méthode fonctionne même si le dossier nommé dans le paramètre _lpszFolderName_ existe déjà en ouvrant le dossier existant qui porte ce nom. Notez que les fournisseurs de magasins de message qui autorisent frère dossiers à avoir le même nom peuvent ouvrir pas dans un dossier existant si plusieurs existe avec le nom fourni. 
    
 _lppFolder_
  
> [out] Pointeur vers un pointeur vers le nouveau dossier.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau dossier a été créé ou ouvert, si l’indicateur OPEN_IF_EXISTS est défini.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_COLLISION 
  
> Il existe un dossier qui porte le nom indiqué dans le paramètre _lpszFolderName_ déjà. Les noms de dossier doivent être uniques. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CreateFolder** crée un sous-dossier dans le dossier actif et affecte un identificateur d’entrée pour le nouveau dossier. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

**CreateFolder** retourne, sachez que l’identificateur d’entrée pour le nouveau dossier ne soit pas disponible. Certains fournisseurs de banque de messages n’apportez identificateurs d’entrée disponibles qu’une fois que vous avez appelé la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du nouveau dossier pour enregistrer de façon permanente. Ceci est particulièrement vrai si vous avez défini l’indicateur MAPI_DEFERRED_ERRORS. 
  
Sachez que certains fournisseurs de banque de messages toujours pointent le paramètre _lppFolder_ interface standard du dossier, quelle que soit la valeur que vous passez dans le paramètre _lpInterface_ . Étant donné que le pointeur d’interface qui est retourné peuvent ne pas être du type que vous attendez, appelez la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) du nouveau dossier pour récupérer la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si nécessaire, effectuer un cast du pointeur vers un type plus approprié avant d’effectuer d’autres appels.
  
La plupart des fournisseurs de banque de messages nécessitent le nom du nouveau dossier unique en ce qui concerne les noms de ses dossiers frères. Être en mesure de gérer la valeur d’erreur MAPI_E_COLLISION, qui est renvoyée si cette règle n’est pas appliquée. 
  
Pour déterminer l’identificateur d’entrée du dossier nouvellement créé, appelez la méthode de **IMAPIProp::GetProps** du nouveau dossier pour récupérer la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI utilise la méthode **CMsgStoreDlg::OnCreateSubFolder** pour créer de nouveaux dossiers de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

