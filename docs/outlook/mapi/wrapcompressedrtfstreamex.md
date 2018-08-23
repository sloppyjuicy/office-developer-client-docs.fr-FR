---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4b7e59c9ffccb2e063962b2cc4947b4fa54757bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572717"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décompresse la le corps d’un message électronique qui est dans compressé texte enrichi (RTF), indique le format de l’objet stream décompressé, si vous le souhaitez convertit le flux décompressé dans son format natif et retourne le flux de données décompressé ou conversion en flux natif.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |Msmapi32.dll  <br/> |
|Appelée par :  <br/> |Client  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Paramètres

_lpCompressedRTFStream_
  
> [in] Il s’agit d’un pointeur vers un flux qui est ouvert sur la [Propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) d’un message. 
    
_pWCSInfo_
  
> [in] Il s’agit d’un pointeur vers un 
    
   Structure [RTF_WCSINFO](rtf_wcsinfo.md) qui contient les options de la fonction. 
    
_lppUncompressedRTFStream_
  
> [out] Il s’agit d’un pointeur vers l’emplacement où un flux pour le format RTF décompressé est retourné. 
    
_pRetInfo_
  
> [out] Il s’agit d’un pointeur vers une structure [RTF_WCSRETINFO](rtf_wcsretinfo.md) qui contient des informations sur le format du flux décompressé renvoyée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L’appel de fonction a réussi.
    
MAPI_E_INVALID_PARAMETER 
  
- Il est renvoyé si l’indicateur **MAPI_NATIVE_BODY** est combiné avec l’indicateur **ne** dans le champ **ulFlags** de la structure **RTF_WCSINFO** sur laquelle pointé *pWCSInfo* . 
    
## <a name="remarks"></a>Remarques

**WrapCompressedRTFStreamEx** permet d’accéder au corps d’un message électronique encapsulé au format RTF compressé par décompression du flux, retourne le flux décompressé et son format et éventuellement le flux du corps native. Le flux du corps native peut être dans le format RTF, texte brut ou HTML. 
  
Le modèle objet Microsoft Office Outlook fournit une propriété **Body** pour les objets **MailItem** et d’une [Propriété MailItem.BodyFormat (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) qui indique le format du corps de texte. Par leur conception, une solution qui n’est pas approuvée par Outlook appelle des boîtes de dialogue de sécurité générés par l’agent de sécurité Outlook. À l’aide de la fonction MAPI exportée **WrapCompressedRTFStreamEx** permet une solution utilisent MAPI au lieu du modèle objet Outlook et d’éviter ces boîtes de dialogue de sécurité. 
  
Étant donné que la **MAPI\_NATIVE_BODY** indicateur ne peut être combiné avec la **MAPI\_modifier** indicateur dans le champ **ulFlags** de la **RTF\_WCSINFO** structure sur laquelle pointe *pWCSInfo*, vous pouvez uniquement accéder natif flux de corps en mode lecture seule. Pour accéder au flux de corps native en mode lecture/écriture, vous devez utiliser la fonction **WrapCompressedRTFStream** . 
  
## <a name="see-also"></a>Voir aussi

- [Récupérer le corps d’un message dans un fichier RTF compressé et le convertir dans son format natif](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

