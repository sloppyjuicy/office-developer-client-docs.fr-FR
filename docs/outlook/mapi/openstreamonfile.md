---
title: OpenStreamOnFile
description: OpenStreamOnFile alloue et initialise un objet OLE IStream pour accéder au contenu d’un fichier. Cette fonction prend une chaîne ANSI comme nom de fichier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
ms.openlocfilehash: 794cef5bbb2f20cfbd1270d6ac26b9198a3a14fd
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852963"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

**S’applique à** : Outlook 2013 | Outlook 2016
  
Alloue et initialise un objet OLE **IStream** pour accéder au contenu d’un fichier. Cette fonction prend une chaîne ANSI comme nom de fichier, y compris le chemin d’accès et l’extension de fichier. Par conséquent, l’utilisation de la version Unicode de cette fonction, [OpenStreamOnFileW](openstreamonfilew.md), est recommandée.
  
|**Élément**|**Valeur**|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |

```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Paramètres

 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.

 _ulFlags_
  
> [in] Masque de bits des indicateurs utilisés pour contrôler la création ou l’ouverture du fichier à accéder via l’objet OLE **IStream** . Les indicateurs suivants peuvent être définis :

SOF_UNIQUEFILENAME
  
> Un fichier temporaire doit être créé pour l’objet **IStream** . Si cet indicateur est défini, les indicateurs STGM_CREATE et STGM_READWRITE doivent également être définis.

STGM_CREATE
  
> Le fichier doit être créé même s’il en existe déjà un. Si le paramètre  _lpszFileName_ n’est pas défini, cet indicateur et STGM_DELETEONRELEASE doivent être définis. Si STGM_CREATE est défini, l’indicateur STGM_READWRITE doit également être défini.

STGM_DELETEONRELEASE
  
> Le fichier doit être supprimé lors de la publication de l’objet **IStream** . Si le paramètre  _lpszFileName_ n’est pas défini, cet indicateur et STGM_CREATE doivent être définis.

STGM_READ
  
> Le fichier doit être créé ou ouvert avec un accès en lecture seule.

STGM_READWRITE
  
> Le fichier doit être créé ou ouvert avec l’autorisation de lecture/écriture. Si cet indicateur n’est pas défini, l’indicateur STGM_CREATE ne doit pas être défini non plus.

 _lpszFileName_
  
> [in] Nom de fichier, y compris le chemin d’accès et l’extension, du fichier pour lequel **OpenStreamOnFile** initialise l’objet **IStream** . Si l’indicateur SOF_UNIQUEFILENAME est défini, _lpszFileName_ contient le chemin d’accès au répertoire dans lequel créer un fichier temporaire. Si  _lpszFileName_ a la valeur NULL, **OpenStreamOnFile** obtient un chemin approprié à partir du système, et les indicateurs STGM_CREATE et STGM_DELETEONRELEASE doivent être définis.

 _lpszPrefix_
  
> [in] Préfixe du nom de fichier sur lequel **OpenStreamOnFile** initialise l’objet **IStream** . S’il est défini, le préfixe ne doit pas contenir plus de trois caractères. Si  _lpszPrefix_ a la valeur NULL, un préfixe « SOF » est utilisé.

 _lppStream_
  
> [out] Pointeur vers un pointeur vers un objet exposant l’interface **IStream** .

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_NO_ACCESS
  
> Impossible d’accéder au fichier en raison d’autorisations utilisateur insuffisantes ou parce que les fichiers en lecture seule ne peuvent pas être modifiés.

MAPI_E_NOT_FOUND
  
> Le fichier désigné n’existe pas.

## <a name="remarks"></a>Remarques

La fonction **OpenStreamOnFile** a deux utilisations importantes, qui se distinguent par le paramètre de l’indicateur SOF_UNIQUEFILENAME. Lorsque cet indicateur n’est pas défini, **OpenStreamOnFile** ouvre un objet **IStream** sur un fichier existant, par exemple pour copier son contenu dans la **propriété PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d’une pièce jointe à l’aide de la méthode **IStream::CopyTo** . Dans ce cas, le paramètre _lpszFileName_ spécifie le chemin d’accès et le nom de fichier du fichier.
  
Lorsque SOF_UNIQUEFILENAME est défini, **OpenStreamOnFile** crée un fichier temporaire pour stocker les données d’un objet **IStream** . Pour cette utilisation, le paramètre _lpszFileName_ peut éventuellement désigner le chemin d’accès au répertoire où le fichier doit être créé, et le paramètre  _lpszPrefix_ peut éventuellement spécifier un préfixe pour le nom de fichier.
  
Lorsque l’application cliente appelante ou le fournisseur de services a terminé avec l’objet **IStream** , il doit le libérer en appelant la méthode OLE **IStream::Release** .
  
MAPI utilise les fonctions pointées par _lpAllocateBuffer_ et _lpFreeBuffer_ pour la plupart de l’allocation et de la désallocation de la mémoire, en particulier pour allouer de la mémoire à utiliser par les applications clientes lors de l’appel d’interfaces d’objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

L’indicateur SOF_UNIQUEFILENAME est utilisé pour créer un fichier temporaire avec un nom propre au système de messagerie. Si cet indicateur est défini, le paramètre _lpszFileName_ spécifie le chemin du fichier temporaire, et le paramètre _lpszPrefix_ contient les caractères de préfixe du nom de fichier. Le nom de fichier construit est \<prefix>HHHH. TMP, où HHHH est un nombre hexadécimal. Si _lpszFileName_ a la valeur NULL, le fichier est créé dans le répertoire de fichiers temporaire retourné par la fonction Windows **GetTempPath**, ou dans le répertoire actif si aucun répertoire de fichiers temporaire n’a été désigné.
  
Si l’indicateur SOF_UNIQUEFILENAME n’est pas défini, _lpszPrefix_ est ignoré et _lpszFileName_ doit contenir le chemin complet et le nom de fichier du fichier à ouvrir ou à créer. Le fichier est ouvert ou créé en fonction des autres indicateurs définis dans _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI utilise la méthode **OpenStreamOnFile** pour ouvrir un flux sur un fichier afin qu’une pièce jointe puisse y être écrite. |

## <a name="see-also"></a>Voir aussi

[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
