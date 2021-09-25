---
title: Propriété canonique PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b4d8d6c3820d0e2954f556f6217cacc1f1a0ea2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571212"
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
  
Les magasins de messages qui prendre en charge le format RTF (Rich Text Format) ignorent les modifications apportées aux espaces dans le texte du message. Lorsque **PR_BODY** est stocké pour la première fois, la boutique de messages génère et stocke également la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF du texte du message. Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée et **que PR_BODY a** été modifié, la boutique de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF. Si seuls des espaces ont été modifiés, les propriétés restent inchangées. Cela permet de conserver toute mise en forme RTF nontrivial lorsque le message passe par des clients et des systèmes de messagerie non RTF. 
  
La valeur de cette propriété doit être exprimée dans la page de code du système d’exploitation sur qui MAPI s’exécute. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

