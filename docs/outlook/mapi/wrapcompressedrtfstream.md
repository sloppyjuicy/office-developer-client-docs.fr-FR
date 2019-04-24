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
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325626"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un flux de texte au format RTF non compressé à partir du format compressé utilisé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
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
  
> dans Pointeur vers un flux ouvert sur la propriété PR_RTF_COMPRESSED d'un message. 
    
 _ulFlags_
  
> dans Masque de masque des indicateurs d'option pour la fonction. Les indicateurs suivants peuvent être définis:
    
MAPI_MODIFY 
  
> Indique si le client envisage de lire ou d'écrire l'interface de flux encapsulé qui est renvoyée. 
    
STORE_UNCOMPRESSED_RTF 
  
> Le format RTF non compressé doit être écrit dans le flux vers lequel pointe _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> remarquer Pointeur vers l'emplacement où **WrapCompressedRTFStream** renvoie un flux pour le format RTF non compressé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Si l'indicateur MAPI_MODIFY est transmis dans le paramètre _ulFlags_ , le paramètre _lpCompressedRTFStream_ doit déjà être ouvert en lecture et en écriture. Le nouveau texte RTF non compressé doit être écrit dans l'interface de flux renvoyée dans _lpUncompressedRTFStream_. Étant donné qu'il n'est pas possible d'ajouter le flux existant, le texte du message entier doit être écrit. 
  
Si la valeur de zéro est transmise au paramètre _ulFlags_ , _lpCompressedRTFStream_ peut être ouvert en lecture seule. Seul le texte du message entier peut être lu à partir de l'interface de flux renvoyée dans _lpUncompressedRTFStream_. Il n'est pas possible d'effectuer une recherche à partir du milieu du flux. 
  
 **WrapCompressedRTFStream** part du principe que le pointeur du flux compressé est défini au début du flux. Certaines méthodes OLE **IStream** ne sont pas prises en charge par le flux non compressé renvoyé. Il s'agit notamment de **IStream:: Clone**, **IStream:: LockRegion**, **IStream:: Revert**, **IStream:: Seek**, **IStream:: assets**, **IStream:: stat**et **IStream:: UnlockRegion**. Pour copier dans le flux entier, une boucle en lecture/écriture est nécessaire. 
  
Étant donné que le client écrit le nouveau format RTF sous une forme non compressée, il doit utiliser **WrapCompressedRTFStream**, au lieu d'écrire directement dans le flux. Les clients prenant en charge le format RTF doivent Rechercher l'indicateur STORE_UNCOMPRESSED_RTF dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) et le transmettre à **WrapCompressed RTFStream** s'il est défini. 
  
## <a name="see-also"></a>Voir aussi



[RTFSync](rtfsync.md)

