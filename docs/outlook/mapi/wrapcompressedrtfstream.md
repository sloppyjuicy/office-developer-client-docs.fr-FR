---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9025bcebdd5e656070b31cd82e6519166a3e3791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787496"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**S’applique à**: Outlook 
  
Crée un flux de texte dans décompressé texte enrichi (RTF) au format compressé utilisée dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Paramètres

 _lpCompressedRTFStream_
  
> [in] Pointeur vers un objet stream ouvert sur la propriété PR_RTF_COMPRESSED d’un message. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs d’option de la fonction. Les indicateurs suivants peuvent être définis :
    
N' 
  
> Si le client a l’intention de lire ou écrire l’interface de flux encapsulé est renvoyée. 
    
STORE_UNCOMPRESSED_RTF 
  
> RTF décompressé doit être écrits dans le flux vers lequel pointé _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [out] Pointeur vers l’emplacement où **WrapCompressedRTFStream** renvoie un flux de données pour le format RTF décompressé. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Si l’indicateur n’est passé dans le paramètre _ulFlags_ , le paramètre _lpCompressedRTFStream_ doit déjà être ouvert pour la lecture et écriture. Nouveau texte RTF décompressé doit être écrits dans l’interface de flux de données retournée dans _lpUncompressedRTFStream_. Car il n’est pas possible d’ajouter le flux existant, le texte de l’intégralité du message doit être écrite. 
  
Si la valeur zéro est transmise dans le paramètre _ulFlags_ , _lpCompressedRTFStream_ peut être ouvert en lecture seule. Seul le texte de l’intégralité du message peut être lue en dehors de l’interface de flux de données retournée dans _lpUncompressedRTFStream_. Il n’est pas possible de rechercher le démarrage du milieu de l’objet stream. 
  
 **WrapCompressedRTFStream** suppose que le pointeur du flux compressé est définie au début de l’objet stream. Certaines méthodes OLE **IStream** ne sont pas pris en charge par le flux non compressé retourné. Cela inclut les **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**et **IStream::UnlockRegion**. Pour pouvoir la copier sur l’intégralité du flux, une boucle de lecture/écriture est nécessaire. 
  
Étant donné que le client écrit nouveau RTF au format non compressé, elle doit utiliser **WrapCompressedRTFStream**, au lieu d’écrire directement dans le flux. Clients prenant en charge les RTF doivent rechercher l’indicateur STORE_UNCOMPRESSED_RTF dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) et passez-le à **WrapCompressed RTFStream** si elle est définie. 
  
## <a name="see-also"></a>Voir aussi



[RTFSync](rtfsync.md)

