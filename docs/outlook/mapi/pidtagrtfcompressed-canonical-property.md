---
title: Propriété canonique PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357889"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propriété canonique PidTagRtfCompressed

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la version RTF (Rich Text Format) du texte du message, généralement sous forme compressée. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificateur :  <br/> |0x1009  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient le même texte de message que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mais au format RTF. 
  
Le texte du message au format RTF est normalement stocké sous forme compressée. Toutefois, certains systèmes ne compressent pas le texte mis en forme. Pour les gérer, MAPI fournit la valeur dwMagicUncompressedRTF pour un en-tête de flux afin d'identifier le format RTF non compressé et l'indicateur **STORE_UNCOMPRESSED_RTF** dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour le message. Store pour indiquer qu'il peut stocker le format RTF non compressé. 
  
Pour obtenir le contenu de cette propriété, appelez **OpenProperty**, puis appelez [WrapCompressedRTFStream](wrapcompressedrtfstream.md) avec l'indicateur **MAPI_READ** . Pour écrire dans cette propriété, ouvrez-la à l'aide des indicateurs **MAPI_MODIFY** et **MAPI_CREATE** . Cela permet de s'assurer que les nouvelles données remplacent entièrement les anciennes données et que les écritures sont effectuées à l'aide du nombre minimal de mises à jour de la Banque. 
  
Les banques de messages qui prennent en charge le format RTF ignorent les modifications apportées aux espaces dans le texte du message. Lorsque **PR_BODY** est stocké pour la première fois, la Banque de messages génère et stocke également cette propriété. Si la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelée par la suite et que **PR_BODY** a été modifié, la Banque de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF. Si seul un espace blanc a été modifié, les propriétés restent inchangées. Cela préserve toute mise en forme RTF non triviale lorsque le message transite par des clients et des systèmes de messagerie qui ne sont pas compatibles avec le format RTF. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Encode et décode un flux compressé dans le corps des messages RTF.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> EnCapsule des formats de contenu supplémentaires (par exemple, HTML) au sein de la propriété de corps RTF des messages et des pièces jointes.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

