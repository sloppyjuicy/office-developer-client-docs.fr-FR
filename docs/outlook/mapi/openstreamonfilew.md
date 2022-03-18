---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: Alloue et initialise un objet OLE IStream pour accéder au contenu d’un fichier.
ms.openlocfilehash: 9dddbc61810f92295c2a9204ae653b3d3d4bda2c
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558361"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

**S’applique à** : Outlook 2013 | Outlook 2016
  
Alloue et initialise un objet OLE **IStream** pour accéder au contenu d’un fichier. Cette fonction prend les chaînes UNICODE comme arguments, contrairement à la version ANSI de cette fonction [OpenStreamOnFile](openstreamonfile.md), et autorise donc les caractères arbitraires dans le nom de fichier, y compris le chemin d’accès et l’extension de fichier.
  
|**Informations**|**Valeur**|
|:-----|:-----|
|Exporté par :  <br/> |olmapi32.dll  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |

```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Paramètres

 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.

 _ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler la création ou l’ouverture du fichier à accéder via l’objet OLE **IStream** . Les indicateurs suivants peuvent être définies :

SOF_UNIQUEFILENAME
  
> Un fichier temporaire doit être créé pour **l’objet IStream** . Si cet indicateur est définie, les STGM_CREATE et STGM_READWRITE doivent également être définies.

STGM_CREATE
  
> Le fichier doit être créé même s’il en existe déjà un. Si le _paramètre lpszFileName n’est_ pas paramétré, cet indicateur et STGM_DELETEONRELEASE être définies. Si STGM_CREATE est définie, l’STGM_READWRITE doit également être définie.

STGM_DELETEONRELEASE
  
> Le fichier doit être supprimé lorsque **l’objet IStream** est libéré. Si le _paramètre lpszFileName n’est_ pas paramétré, cet indicateur et STGM_CREATE être définies.

STGM_READ
  
> Le fichier doit être créé ou ouvert avec un accès en lecture seule.

STGM_READWRITE
  
> Le fichier doit être créé ou ouvert avec une autorisation de lecture/écriture. Si cet indicateur n’est pas définie, l’STGM_CREATE ne doit pas non plus être définie.

 _lpszFileName_
  
> [in] Nom du fichier, y compris le chemin d’accès et l’extension, du fichier nommé Unicode pour lequel **OpenStreamOnFileW** initialise **l’objet IStream** . Si l SOF_UNIQUEFILENAME est définie, _lpszFileName_ contient le chemin d’accès au répertoire dans lequel créer un fichier temporaire. Si _lpszFileName_ est NULL, **OpenStreamOnFileW** obtient un chemin d’accès approprié à partir du système et les indicateurs STGM_CREATE et STGM_DELETEONRELEASE doivent être définies.

 _lpszPrefix_
  
> [in] Préfixe du nom de fichier Unicode sur lequel **OpenStreamOnFileW** initialise **l’objet IStream** . S’il est définie, le préfixe ne doit pas contenir plus de trois caractères. Si _lpszPrefix_ a la valeur NULL, un préfixe « SOF » est utilisé.

 _lppStream_
  
> [out] Pointeur vers un pointeur vers un objet exposant l’interface **IStream** .

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_NO_ACCESS
  
> Le fichier n’a pas pu être accessible en raison d’autorisations utilisateur insuffisantes ou parce que les fichiers en lecture seule ne peuvent pas être modifiés.

MAPI_E_NOT_FOUND
  
> Le fichier désigné n’existe pas.

## <a name="remarks"></a>Remarques

La **fonction OpenStreamOnFileW** a deux utilisations importantes en plus de la gestion d’un fichier avec un nom Unicode, qui se distingue par le paramètre de l’indicateur SOF_UNIQUEFILENAME. Lorsque cet indicateur n’est pas définie, **OpenStreamOnFileW** ouvre un objet **IStream** sur un fichier existant, par exemple pour copier son contenu dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d’une pièce jointe à l’aide de la méthode **IStream::CopyTo** . Dans ce cas, _le paramètre lpszFileName_ spécifie le chemin d’accès et le nom du fichier.
  
Lorsque SOF_UNIQUEFILENAME est définie, **OpenStreamOnFileW** crée un fichier temporaire pour contenir les données **d’un objet IStream** . Pour cette utilisation, le paramètre _lpszFileName_ peut éventuellement désigner le chemin d’accès au répertoire dans lequel le fichier doit être créé, et le paramètre _lpszPrefix_ peut éventuellement spécifier un préfixe pour le nom de fichier.
  
Lorsque l’application cliente ou le fournisseur de services appelant est terminé avec l’objet **IStream** , il doit le libérer en appelant la méthode OLE **IStream::Release** .
  
MAPI utilise les fonctions pointées par _lpAllocateBuffer_ et _lpFreeBuffer_ pour la plupart de l’allocation et de la déallocation de la mémoire, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

L SOF_UNIQUEFILENAME est utilisé pour créer un fichier temporaire avec un nom propre au système de messagerie. Si cet indicateur est définie, le paramètre _lpszFileName_ specifes the path for the temporary file, and the _lpszPrefix_ parameter contains the prefix characters of the filename. Le nom de fichier construit est \<prefix>HHHH. TMP, où HHHH est un nombre hexadécimal. Si _lpszFileName_ est NULL, le fichier est créé dans le répertoire de fichiers temporaire qui est renvoyé à partir de la fonction Windows **GetTempPath**, ou le répertoire actuel si aucun répertoire de fichiers temporaires n’a été désigné.
  
Si l’indicateur SOF_UNIQUEFILENAME n’est pas définie, _lpszPrefix_ est ignoré et _lpszFileName_ doit contenir le chemin d’accès complet et le nom du fichier à ouvrir ou à créer. Le fichier sera ouvert ou créé en fonction des autres indicateurs qui sont définies dans _ulFlags_.
  
## <a name="see-also"></a>Voir aussi

[OpenStreamOnFile](openstreamonfile.md)
