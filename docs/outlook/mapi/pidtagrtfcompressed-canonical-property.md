---
title: Propriété canonique PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: Contient la version RTF (Rich Text Format) du texte du message, généralement sous forme compressée pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 616dc0d8250815a99dcdafe8cda58e1c7d21b85c
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524075"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propriété canonique PidTagRtfCompressed

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la version RTF (Rich Text Format) du texte du message, généralement sous forme compressée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificateur :  <br/> |0x1009  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient le même texte de message que **la propriété PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mais au niveau rtf. 
  
Le texte du message au niveau rtf est normalement stocké sous forme compressée. Toutefois, certains systèmes ne compressent pas le texte formaté. Pour les prendre en charge, MAPI fournit la valeur dwMagicUncompressedRTF pour un en-tête de flux afin d’identifier le RTF non compressé et l’indicateur **STORE_UNCOMPRESSED_RTF** dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour la magasin de messages pour indiquer qu’il peut stocker un RTF non compressé. 
  
Pour obtenir le contenu de cette propriété, appelez **OpenProperty**, puis appelez [WrapCompressedRTFStream](wrapcompressedrtfstream.md) avec **l’MAPI_READ’indicateur** . Pour écrire dans cette propriété, ouvrez-la avec **MAPI_MODIFY et** **MAPI_CREATE** indicateurs. Cela garantit que les nouvelles données remplacent complètement les anciennes données et que les écritures sont effectuées à l’aide du nombre minimal de mises à jour de la boutique. 
  
Les magasins de messages qui la prise en charge rtf ignorent les modifications apportées aux espaces dans le texte du message. Lorsque **PR_BODY** est stocké pour la première fois, la boutique de messages génère et stocke également cette propriété. Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée et que **PR_BODY a** été modifié, la boutique de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF. Si seuls des espaces ont été modifiés, les propriétés restent inchangées. Cela permet de conserver toute mise en forme RTF nontrivial lorsque le message passe par des clients et des systèmes de messagerie non RTF. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Encode et décode un flux compressé dans les corps des messages RTF.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Encapsule les formats de contenu supplémentaires (par exemple, HTML) dans la propriété rtF body des messages et des pièces jointes.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

