---
title: IMAPIFolderCreateFolder
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 67691f49f84bf3a49ca9cca4a6cab7c76228e6b7
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464823"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un sous-ensemble.
  
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
  
> [in] Type de dossier à créer. Les indicateurs suivants peuvent être définies :
    
FOLDER_GENERIC 
  
> Un dossier générique doit être créé.
    
FOLDER_SEARCH 
  
> Un dossier de résultats de recherche doit être créé.
    
 _lpszFolderName_
  
> [in] Pointeur vers une chaîne qui contient le nom du nouveau dossier. Ce nom est la base de la propriété **PR_DISPLAY_NAME (**[PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du nouveau dossier.
    
 _lpszFolderComment_
  
> [in] Pointeur vers une chaîne qui contient un commentaire associé au nouveau dossier. Cette chaîne devient la valeur de la propriété **PR_COMMENT (**[PidTagComment](pidtagcomment-canonical-property.md)) du nouveau dossier. Si la valeur NULL est passée, le dossier n’a pas de commentaire initial.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau dossier. Si la valeur NULL est passé, le fournisseur de magasin de messages retourne l’interface de dossier standard [, IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent passer la valeur NULL. D’autres appelants peuvent définir le paramètre  _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est créé. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **CreateFolder de renvoyer** correctement, éventuellement avant que le nouveau dossier soit entièrement disponible pour le client appelant. Si le nouveau dossier n’est pas disponible, un appel ultérieur peut provoquer une erreur. 
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.
    
OPEN_IF_EXISTS 
  
> Permet à la méthode de réussir même si le dossier nommé dans le paramètre _lpszFolderName_ existe déjà en ouvrant le dossier existant portant ce nom. Notez que les fournisseurs de magasins de messages qui autorisent les dossiers frères à avoir le même nom peuvent ne pas ouvrir un dossier existant s’il en existe plusieurs avec le nom fourni. 
    
 _lppFolder_
  
> [out] Pointeur vers un pointeur vers le dossier nouvellement créé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau dossier a été créé ou ouvert, si l’OPEN_IF_EXISTS est définie.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_COLLISION 
  
> Un dossier dont le nom est donné dans le _paramètre lpszFolderName_ existe déjà. Les noms de dossier doivent être uniques. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::CreateFolder** crée un sous-dossier dans le dossier actuel et affecte un identificateur d’entrée au nouveau dossier. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **CreateFolder est** de retour, sachez que l’identificateur d’entrée pour le nouveau dossier n’est peut-être pas disponible. Certains fournisseurs de magasins de messages ne rendent les identificateurs d’entrée disponibles qu’après avoir appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du nouveau dossier pour l’enregistrer définitivement. Cela est particulièrement vrai si vous avez MAPI_DEFERRED_ERRORS’indicateur. 
  
Sachez que certains fournisseurs de magasins de messages pointent toujours le paramètre  _lppFolder_ vers l’interface standard du dossier, quelle que soit la valeur que vous passez pour le paramètre  _lpInterface_ . Étant donné que le pointeur d’interface renvoyé peut ne pas être du type prévu, appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du nouveau dossier pour récupérer la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si nécessaire,  castez le pointeur vers un type plus approprié avant d’effectuer d’autres appels.
  
La plupart des fournisseurs de magasins de messages exigent que le nom du nouveau dossier soit unique par rapport aux noms de ses dossiers frères. Être en mesure de gérer la valeur MAPI_E_COLLISION’erreur, qui est renvoyée si cette règle n’est pas suivie. 
  
Pour déterminer l’identificateur d’entrée du dossier nouvellement créé, appelez la méthode **IMAPIProp::GetProps** du nouveau dossier pour récupérer sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI utilise **la méthode CMsgStoreDlg::OnCreateSubFolder** pour créer des dossiers dans MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

