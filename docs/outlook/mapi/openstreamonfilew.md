---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406023"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Alloue et initialise un objet OLE **IStream** pour accéder au contenu d'un fichier. Cette fonction prend des chaînes UNICODE comme arguments, contrairement à la version ANSI de cette fonction [OpenStreamOnFile](openstreamonfile.md), et permet donc des caractères arbitraires dans le nom de fichier, y compris le chemin d'accès et l'extension de fichier.
  
|||
|:-----|:-----|
|Exporté par:  <br/> |olmapi32. dll  <br/> |
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
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _ulFlags_
  
> dans Masque de réinitialisation des indicateurs utilisés pour contrôler la création ou l'ouverture du fichier accessible par le biais de l'objet OLE **IStream** . Les indicateurs suivants peuvent être définis: 
    
SOF_UNIQUEFILENAME
  
> Un fichier temporaire doit être créé pour l'objet **IStream** . Si cet indicateur est défini, les indicateurs STGM_CREATE et STGM_READWRITE doivent également être définis. 
    
STGM_CREATE
  
> Le fichier doit être créé même s'il en existe déjà un. Si le paramètre _lpszFileName_ n'est pas défini, cet indicateur et STGM_DELETEONRELEASE doivent être définis. Si STGM_CREATE est défini, l'indicateur STGM_READWRITE doit également être défini. 
    
STGM_DELETEONRELEASE
  
> Le fichier doit être supprimé lors de la publication de l'objet **IStream** . Si le paramètre _lpszFileName_ n'est pas défini, cet indicateur et STGM_CREATE doivent être définis. 
    
STGM_READ
  
> Le fichier doit être créé ou ouvert avec un accès en lecture seule.
    
STGM_READWRITE
  
> Le fichier doit être créé ou ouvert avec une autorisation en lecture/écriture. Si cet indicateur n'est pas défini, l'indicateur STGM_CREATE ne doit pas être défini.
    
 _lpszFileName_
  
> dans Nom de fichier, y compris le chemin d'accès et l'extension, du fichier nommé Unicode pour lequel **OpenStreamOnFileW** Initialise l'objet **IStream** . Si l'indicateur SOF_UNIQUEFILENAME est défini, _lpszFileName_ contient le chemin d'accès au répertoire dans lequel créer un fichier temporaire. Si _lpszFileName_ a la valeur null, **OpenStreamOnFileW** obtient un chemin d'accès approprié à partir du système, et les indicateurs STGM_CREATE et STGM_DELETEONRELEASE doivent être définis. 
    
 _lpszPrefix_
  
> dans Préfixe du nom de fichier Unicode sur lequel **OpenStreamOnFileW** Initialise l'objet **IStream** . Si ce paramètre est défini, le préfixe ne doit pas comporter plus de trois caractères. Si _lpszPrefix_ est null, le préfixe «SOF» est utilisé. 
    
 _lppStream_
  
> remarquer Pointeur vers un pointeur vers un objet qui expose l'interface **IStream** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_ACCESS
  
> Le fichier n'est pas accessible car les autorisations utilisateur sont insuffisantes ou les fichiers en lecture seule ne peuvent pas être modifiés.
    
MAPI_E_NOT_FOUND
  
> Le fichier désigné n'existe pas.
    
## <a name="remarks"></a>Remarques

La fonction **OpenStreamOnFileW** a deux utilisations importantes en plus de la gestion d'un fichier avec un nom Unicode, distingué par le paramètre de l'indicateur SOF_UNIQUEFILENAME. Lorsque cet indicateur n'est pas défini, **OpenStreamOnFileW** ouvre un objet **IStream** sur un fichier existant, par exemple pour copier son contenu dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d'une pièce jointe à l'aide de la **balise IStream:: CopyTo** , méthode. Dans ce cas, le paramètre _lpszFileName_ spécifie le chemin d'accès et le nom du fichier. 
  
Lorsque SOF_UNIQUEFILENAME est défini, **OpenStreamOnFileW** crée un fichier temporaire pour conserver les données d'un objet **IStream** . Pour cette utilisation, le paramètre _lpszFileName_ peut éventuellement désigner le chemin d'accès au répertoire dans lequel le fichier doit être créé et le paramètre _lpszPrefix_ peut éventuellement spécifier un préfixe pour le nom de fichier. 
  
Lorsque l'application cliente ou le fournisseur de services appelant est terminé avec l'objet **IStream** , il doit le libérer en appelant la méthode OLE **IStream:: Release** . 
  
MAPI utilise les fonctions pointées par _lpAllocateBuffer_ et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire, notamment pour allouer de la mémoire aux applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

L'indicateur SOF_UNIQUEFILENAME est utilisé pour créer un fichier temporaire avec un nom unique pour le système de messagerie. Si cet indicateur est défini, le paramètre _lpszFileName_ spécifie le chemin d'accès au fichier temporaire et le paramètre _lpszPrefix_ contient les caractères de préfixe du nom de fichier. Le nom de fichier <prefix>construit est hhhh. TMP, où HHHH est un nombre hexadécimal. Si _lpszFileName_ a la valeur null, le fichier est créé dans le répertoire de fichiers temporaires renvoyé à partir de la fonction **GetTempPath**de Windows ou du répertoire actif si aucun répertoire de fichiers temporaire n'a été désigné.
  
Si l'indicateur SOF_UNIQUEFILENAME n'est pas défini, _lpszPrefix_ est ignoré et _lpszFileName_ doit contenir le chemin d'accès complet et le nom de fichier du fichier à ouvrir ou à créer. Le fichier est ouvert ou créé en fonction des autres indicateurs définis dans _ulFlags_.
  
## <a name="see-also"></a>Voir aussi



[OpenStreamOnFile](openstreamonfile.md)

