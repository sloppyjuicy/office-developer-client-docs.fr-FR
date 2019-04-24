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
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357875"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propriété canonique PidTagRtfInSync

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a le même contenu de texte que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificateur :  <br/> |0x0E1F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur TRUE indique que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la version texte brut de ce message et la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version au format RTF (Rich Text Format), sont identiques, à l'exception de espace blanc dans **PR_BODY** et mise en forme dans **PR_RTF_COMPRESSED**. Le texte dans les deux versions se compose des mêmes caractères dans la même séquence.
  
La valeur FALSe signifie que les deux versions ne sont pas synchronisées pour le contenu de texte, mais qu'elles peuvent être synchronisées par la fonction [RTFSync](rtfsync.md) . Une version a été modifiée et l'autre n'a pas été modifiée. 
  
Aucune valeur signifie que les deux versions, si elles existent ou si elles existaient, ne peuvent pas être synchronisées. Une version a été supprimée ou modifiée si bien que la synchronisation n'est plus possible.
  
Une application cliente qui a modifié **PR_RTF_COMPRESSED** doit définir la valeur false dans cette propriété pour forcer la synchronisation. Les banques de messages prenant en charge le format RTF doivent effectuer la synchronisation à l'aide de **RTFSync** pendant un appel [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Les clients compatibles avec le format RTF doivent vérifier la valeur de **PR_RTF_IN_SYNC** avant de lire **PR_RTF_COMPRESSED**et appeler **RTFSync** d'abord si nécessaire. 
  
Si **PR_BODY** a eu des modifications apportées à d'autres éléments que son espace blanc, la Banque de messages doit supprimer **PR_RTF_IN_SYNC** pour mettre fin à la synchronisation. 
  
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

