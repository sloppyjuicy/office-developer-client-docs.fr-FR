---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325773"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décompresse le corps d’un message électronique au format RTF (Compressed Rich Text Format), indique le format du flux décompressé, convertit éventuellement le flux décompressé en son format natif et renvoie le flux décompressé ou le flux natif converti.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Paramètres

_lpCompressedRTFStream_
  
> [in] Il s’agit d’un pointeur vers un flux ouvert sur la propriété canonique [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) d’un message. 
    
_pWCSInfo_
  
> [in] Il s’agit d’un pointeur vers un 
    
   [RTF_WCSINFO](rtf_wcsinfo.md) structure qui contient les options de la fonction. 
    
_lppUncompressedRTFStream_
  
> [out] Il s’agit d’un pointeur vers l’emplacement où un flux pour le RTF décompressé est renvoyé. 
    
_pRetInfo_
  
> [out] Il s’agit d’un [pointeur vers une](rtf_wcsretinfo.md) structure RTF_WCSRETINFO qui contient des informations sur le format du flux décompressé renvoyé. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L’appel de fonction a réussi.
    
MAPI_E_INVALID_PARAMETER 
  
- Ceci est renvoyé si **l’indicateur MAPI_NATIVE_BODY** est combiné avec l’indicateur **MAPI_MODIFY** dans le champ **ulFlags** de la structure **RTF_WCSINFO** pointée par  *pWCSInfo*  . 
    
## <a name="remarks"></a>Remarques

**WrapCompressedRTFStreamEx** vous permet d’accéder au corps d’un message électronique encapsulé dans un format RTF compressé en décompressant le flux, renvoie le flux décompressé et son format, et éventuellement le flux de corps natif. Le flux de corps natif peut être au format RTF, en texte brut ou au format HTML. 
  
Le Microsoft Office Outlook objet fournit une propriété **Body** pour les objets **MailItem** et une [propriété MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) qui indique le format du corps de texte. Par conception, une solution non fiable par Outlook appelle les boîtes de dialogue de sécurité générées par Outlook Security Guard. L’utilisation de la fonction MAPI **exportée WrapCompressedRTFStreamEx** permet à une solution d’utiliser MAPI au lieu du modèle objet Outlook et d’éviter ces boîtes de dialogue de sécurité. 
  
Étant donné que l’indicateur **\_ NATIVE_BODY MAPI** ne peut pas être combiné avec l’indicateur **MAPI \_ MODIFY** dans le champ **ulFlags** de la structure **\_ WCSINFO RTF** pointée par *pWCSInfo,* vous pouvez uniquement accéder au flux de corps natif en mode lecture seule. Pour accéder au flux de corps natif en mode lecture/écriture, vous devez utiliser la fonction **WrapCompressedRTFStream.** 
  
## <a name="see-also"></a>Voir aussi

- [Récupérer le corps d’un message au format RTF compressé et le convertir au format natif](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

