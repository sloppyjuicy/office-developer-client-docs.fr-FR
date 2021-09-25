---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: af4c5b0305f8de8b31ca54747db2d3faed68131f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609186"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un flux de texte au format RTF (Rich Text Format) non compressé à partir du format compressé utilisé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Paramètres

 _lpCompressedRTFStream_
  
> [in] Pointeur vers un flux ouvert sur la PR_RTF_COMPRESSED d’un message. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs d’option pour la fonction. Les indicateurs suivants peuvent être définies :
    
MAPI_MODIFY 
  
> Si le client a l’intention de lire ou d’écrire l’interface de flux wrapped renvoyée. 
    
STORE_UNCOMPRESSED_RTF 
  
> Uncompressed RTF doit être écrit dans le flux pointé par  _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [out] Pointeur vers l’emplacement où **WrapCompressedRTFStream** renvoie un flux pour le RTF non compressé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Si l MAPI_MODIFY est transmis dans le paramètre  _ulFlags,_ le paramètre  _lpCompressedRTFStream_ doit déjà être ouvert pour la lecture et l’écriture. Le nouveau texte RTF non compressé doit être écrit dans l’interface de flux renvoyée dans  _lpUncompressedRTFStream_. Étant donné qu’il n’est pas possible d’appender le flux existant, l’intégralité du texte du message doit être écrite. 
  
Si zéro est transmis dans le  _paramètre ulFlags,_  _lpCompressedRTFStream_ peut être ouvert en lecture seule. Seul l’intégralité du texte du message peut être lue à partir de l’interface de flux renvoyée dans  _lpUncompressedRTFStream_. Il n’est pas possible de rechercher à partir du milieu du flux. 
  
 **WrapCompressedRTFStream** suppose que le pointeur du flux compressé est placé au début du flux. Certaines méthodes OLE **IStream** ne sont pas pris en charge par le flux non compressé renvoyé. Ceux-ci incluent **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** et **IStream::UnlockRegion**. Pour copier dans le flux entier, une boucle de lecture/écriture est nécessaire. 
  
Étant donné que le client écrit le nouveau format RTF dans un format non compressé, il doit utiliser **WrapCompressedRTFStream**, au lieu d’écrire directement dans le flux. Les clients rtF doivent rechercher l’indicateur STORE_UNCOMPRESSED_RTF dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) et le transmettre à **WrapCompressed RTFStream** s’il est paradé. 
  
## <a name="see-also"></a>Voir aussi



[RTFSync](rtfsync.md)

