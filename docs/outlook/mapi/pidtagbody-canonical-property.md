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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cbcfdf44044e3cf9e42b0f0503928c9f8720ec1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574418"
---
# <a name="pidtagbody-canonical-property"></a>Propriété canonique PidTagBody

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Identificateur :  <br/> |0 x 1000  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont généralement utilisées uniquement dans un message interpersonnel (IPM). 
  
Banques de messages qui prennent en charge le Format RTF (RICH Text Format) ignorent toutes les modifications dans l’espace blanc dans le texte du message. Lorsque **PR_BODY** est stockée pour la première fois, la banque de messages également génère et stocke la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF du texte du message. Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée par la suite et **PR_BODY** a été modifié, la banque de messages appelle la fonction de [RTFSync](rtfsync.md) pour assurer la synchronisation avec la version RTF. Si seule l’espace blanc a été modifié, les propriétés restent inchangées. Ainsi, n’importe quel format RTF important mise en forme lorsque le message transite par non RTF-prenant en charge les clients et les systèmes de messagerie. 
  
La valeur de cette propriété doit être exprimée dans la page de codes du système d’exploitation exécuté sur MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

