---
title: Propriété canonique PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786639"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propriété canonique PidTagRtfInSync

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a le même contenu de texte en tant que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificateur :  <br/> |0x0E1F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Courier électronique  <br/> |
   
## <a name="remarks"></a>Remarques

Valeur TRUE signifie que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la version en texte brut de ce message et la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version du Format RTF (RICH Text Format), sont identiques à l’exception des espace blanc dans **PR_BODY** et la mise en forme **PR_RTF_COMPRESSED**. Le texte dans les deux versions se compose des caractères dans le même ordre.
  
Valeur FALSE signifie que les deux versions ne sont pas synchronisées pour le contenu de texte mais qui sont capables de synchronisés par la fonction [RTFSync](rtfsync.md) . Une version a été modifiée et l’autre version n’a pas. 
  
Aucune valeur ne signifie que les deux versions, si les deux existent ou existaient déjà, ne peuvent pas être synchronisées. Une version a été supprimée ou modifiée radicalement que la synchronisation n’est plus possible.
  
Une application cliente qui a modifié **PR_RTF_COMPRESSED** doit définir la valeur FALSE à cette propriété pour forcer la synchronisation. Banques de messages RTF prenant en charge doivent effectuer la synchronisation à l’aide de **RTFSync** pendant un appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Les clients prenant en charge les RTF doivent vérifier le paramètre de **PR_RTF_IN_SYNC** avant de lire **PR_RTF_COMPRESSED**et **RTFSync** d’abord appeler si nécessaire. 
  
Si **PR_BODY** a eu des modifications à son espace, la banque de messages doit supprimer **PR_RTF_IN_SYNC** pour mettre fin à la synchronisation. 
  
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

