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
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436761"
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
  
> dans Type de dossier à créer. Les indicateurs suivants peuvent être définis:
    
FOLDER_GENERIC 
  
> Un dossier générique doit être créé.
    
FOLDER_SEARCH 
  
> Un dossier de résultats de recherche doit être créé.
    
 _lpszFolderName_
  
> dans Pointeur vers une chaîne qui contient le nom du nouveau dossier. Ce nom est la base de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du nouveau dossier.
    
 _lpszFolderComment_
  
> dans Pointeur vers une chaîne qui contient un commentaire associé au nouveau dossier. Cette chaîne devient la valeur de la propriété **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) du nouveau dossier. Si la valeur NULL est transmise, le dossier n'a pas de commentaire initial.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au nouveau dossier. En passant NULL, le fournisseur de banque de messages renvoie l'interface de dossier standard, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent transmettre la valeur NULL. Les autres appelants peuvent définir le paramètre _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le dossier est créé. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet le renvoi correct de **CreateFolder** , éventuellement avant que le nouveau dossier soit entièrement disponible pour le client appelant. Si le nouveau dossier n'est pas disponible, une erreur peut se produire lors d'un appel ultérieur. 
    
MAPI_UNICODE 
  
> Le nom du dossier est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du dossier est au format ANSI.
    
OPEN_IF_EXISTS 
  
> Autorise la méthode à aboutir même si le dossier nommé dans le paramètre _lpszFolderName_ existe déjà en ouvrant le dossier existant qui porte ce nom. Notez que les fournisseurs de banques de messages qui permettent aux dossiers frères de posséder le même nom peuvent ne pas ouvrir un dossier existant s'il en existe plusieurs avec le nom fourni. 
    
 _lppFolder_
  
> remarquer Pointeur vers un pointeur vers le dossier nouvellement créé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau dossier a été créé ou ouvert avec succès, si l'indicateur OPEN_IF_EXISTS est défini.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
MAPI_E_COLLISION 
  
> Un dossier dont le nom est indiqué dans le paramètre _lpszFolderName_ existe déjà. Les noms de dossier doivent être uniques. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: CreateFolder** crée un sous-dossier dans le dossier actif et affecte un identificateur d'entrée au nouveau dossier. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **CreateFolder** renvoie, Notez que l'identificateur d'entrée pour le nouveau dossier peut ne pas être disponible. Certains fournisseurs de banques de messages ne rendent pas d'identificateurs d'entrée disponibles tant que vous n'avez pas appelé la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du nouveau dossier pour l'enregistrer définitivement. Cela est particulièrement vrai si vous avez défini l'indicateur MAPI_DEFERRED_ERRORS. 
  
N'oubliez pas que certains fournisseurs de banques de messages pointent toujours le paramètre _lppFolder_ vers l'interface standard du dossier, quelle que soit la valeur que vous transmettez pour le paramètre _lpInterface_ . Étant donné que le pointeur d'interface renvoyé n'est peut-être pas du type prévu, appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du nouveau dossier pour extraire la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si nécessaire, effectuez un cast du pointeur vers un type plus approprié avant d'effectuer d'autres appels.
  
La plupart des fournisseurs de banques de messages exigent que le nom du nouveau dossier soit unique par rapport aux noms de ses dossiers frères. Pouvoir gérer la valeur d'erreur MAPI_E_COLLISION, qui est renvoyée si cette règle n'est pas suivie. 
  
Pour déterminer l'identificateur d'entrée du dossier nouvellement créé, appelez la méthode **IMAPIProp:: GetProps** du nouveau dossier pour extraire sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnCreateSubFolder  <br/> |MFCMAPI utilise la méthode **CMsgStoreDlg:: OnCreateSubFolder** pour créer des dossiers dans MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

