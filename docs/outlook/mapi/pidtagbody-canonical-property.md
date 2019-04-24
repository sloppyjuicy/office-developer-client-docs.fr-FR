---
title: Propriété canonique PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326634"
---
# <a name="pidtagbody-canonical-property"></a>Propriété canonique PidTagBody

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Identificateur :  <br/> |0x1000  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont généralement utilisées uniquement dans un message interpersonnel (IPM). 
  
Les banques de messages qui prennent en charge le format RTF (Rich Text Format) ignorent les modifications apportées à l'espace dans le texte du message. Lorsque **PR_BODY** est stocké pour la première fois, la Banque de messages génère et stocke également la propriété **PR_RTF_COMPRESSED** ([PIDTAGRTFCOMPRESSED](pidtagrtfcompressed-canonical-property.md)), la version RTF du texte du message. Si la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelée par la suite et que **PR_BODY** a été modifié, la Banque de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF. Si seul un espace blanc a été modifié, les propriétés restent inchangées. Cela préserve toute mise en forme RTF non triviale lorsque le message transite par des clients et des systèmes de messagerie qui ne sont pas compatibles avec le format RTF. 
  
La valeur de cette propriété doit être exprimée dans la page de code du système d'exploitation sur lequel MAPI est exécuté. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

