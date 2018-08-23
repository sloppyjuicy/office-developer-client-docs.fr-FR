---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9f37e57f997ead58b1ef0e9a27ccbdb0a810be06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571954"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Alloue et initialise un objet OLE **IStream** pour accéder au contenu d’un fichier. Cette fonction accepte une chaîne ANSI comme le nom de fichier, y compris le chemin d’accès et l’extension de fichier, par conséquent, l’utilisation de la version Unicode de cette fonction, [OpenStreamOnFileW](openstreamonfilew.md), est recommandé.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler la création ou l’ouverture du fichier à accessible par le biais de l’objet OLE **IStream** . Les indicateurs suivants peuvent être définis : 
    
SOF_UNIQUEFILENAME 
  
> Un fichier temporaire doit être créé pour l’objet **IStream** . Si cet indicateur est défini, les indicateurs STGM_CREATE et STGM_READWRITE doivent également être définies. 
    
STGM_CREATE 
  
> Le fichier doit être créé même si elle existe déjà. Si le paramètre _lpszFileName_ n’est pas défini, cet indicateur et la STGM_DELETEONRELEASE doivent être définie. Si STGM_CREATE est défini, l’indicateur STGM_READWRITE doit également être définie. 
    
STGM_DELETEONRELEASE 
  
> Le fichier doit être supprimé lors de l’objet **IStream** . Si le paramètre _lpszFileName_ n’est pas défini, cet indicateur et la STGM_CREATE doivent être définie. 
    
STGM_READ 
  
> Le fichier doit être créé ou ouvert avec accès en lecture seule. 
    
STGM_READWRITE 
  
> Le fichier doit être créé ou ouvert avec l’autorisation de lecture/écriture. Si cet indicateur n’est pas défini, l’indicateur STGM_CREATE ne doit pas être définie soit. 
    
 _lpszFileName_
  
> [in] Nom de fichier, y compris le chemin d’accès et l’extension du fichier pour lequel **OpenStreamOnFile** initialise l’objet **IStream** . Si l’indicateur SOF_UNIQUEFILENAME est défini, _lpszFileName_ contient le chemin d’accès au répertoire dans lequel vous souhaitez créer un fichier temporaire. Si _lpszFileName_ est NULL, **OpenStreamOnFile** Obtient un chemin d’accès approprié à partir du système et indicateurs STGM_DELETEONRELEASE et STGM_CREATE doivent être définis. 
    
 _lpszPrefix_
  
> [in] Préfixe de nom de fichier sur lequel **OpenStreamOnFile** initialise l’objet **IStream** . Si défini, le préfixe doit contenir pas plus de trois caractères. Si _lpszPrefix_ est NULL, le préfixe « SOF » est utilisé. 
    
 _lppStream_
  
> [out] Pointeur vers un pointeur vers un objet exposition de l’interface **IStream** . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_NO_ACCESS 
  
> Le fichier est inaccessible en raison d’autorisations insuffisantes utilisateur ou parce que les fichiers en lecture seule ne peut pas être modifiés. 
    
MAPI_E_NOT_FOUND 
  
> Le fichier désigné n’existe pas.
    
## <a name="remarks"></a>Remarques

La fonction **OpenStreamOnFile** a deux utilisations importantes, caractérisées par le paramètre de l’indicateur SOF_UNIQUEFILENAME. Lorsque cet indicateur n’est pas défini, **OpenStreamOnFile** ouvre un objet **IStream** sur un fichier existant, par exemple pour copier son contenu dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d’une pièce jointe à l’aide de la **IStream :: CopyTo** méthode. Dans ce cas, le paramètre _lpszFileName_ Spécifie le chemin d’accès et le nom du fichier. 
  
Lorsque SOF_UNIQUEFILENAME est défini, **OpenStreamOnFile** crée un fichier temporaire pour stocker les données d’un objet **IStream** . Pour cela, le paramètre _lpszFileName_ peut désigner éventuellement le chemin d’accès au répertoire où le fichier doit être créé, et le paramètre _lpszPrefix_ peut éventuellement spécifier un préfixe pour le nom de fichier. 
  
Lorsque l’application cliente appelant ou un fournisseur de services est terminé avec l’objet **IStream** , il doit le libérer en appelant la méthode OLE **IStream::Release** . 
  
MAPI utilise les fonctions désignées par _lpAllocateBuffer_ et _lpFreeBuffer_ pour la plupart de l’allocation de mémoire et de désaffectation, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet tel que [IMAPIProp :: GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

L’indicateur SOF_UNIQUEFILENAME est utilisé pour créer un fichier temporaire avec un nom unique pour le système de messagerie. Si cet indicateur est défini, la spécifie de paramètre _lpszFileName_ le chemin d’accès pour le fichier temporaire et le paramètre _lpszPrefix_ contient les premiers caractères du nom de fichier. Est le nom de fichier construit <prefix>HHHH. TMP, où HHHH est un nombre hexadécimal. Si _lpszFileName_ est NULL, le fichier sera créé dans le répertoire du fichier temporaire qui est renvoyé à partir de la fonction Windows **GetTempPath**ou le répertoire actif si aucun répertoire de fichiers temporaires n’a été désigné. 
  
Si l’indicateur SOF_UNIQUEFILENAME n’est pas définie, _lpszPrefix_ est ignorée et _lpszFileName_ doit contenir le chemin d’accès complet et le nom du fichier à être ouvert ou créé. Le fichier est ouvert ou créé selon les autres indicateurs qui sont définis dans _ulFlags_. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI utilise la méthode **OpenStreamOnFile** pour ouvrir un objet stream dans un fichier peut être écrites une pièce jointe à celui-ci.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

