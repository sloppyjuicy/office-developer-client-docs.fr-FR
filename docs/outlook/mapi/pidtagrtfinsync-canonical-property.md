---
title: Propriété canonique PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 72a94f6063dcc1abd1ca5c17d8bc048baad7953e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604214"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propriété canonique PidTagRtfInSync

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si la **propriété PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a le même contenu de texte que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificateur :  <br/> |0x0E1F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur TRUE signifie que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la version en texte simple de ce message et la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF (Rich Text Format), sont identiques à l’exception des espaces blancs dans **PR_BODY** et de la mise en forme dans **PR_RTF_COMPRESSED**. Le texte des deux versions se compose des mêmes caractères dans la même séquence.
  
La valeur FALSE signifie que les deux versions ne sont pas synchronisées pour le contenu de texte, mais sont capables d’être synchronisées par la [fonction RTFSync.](rtfsync.md) Une version a été modifiée et l’autre version n’a pas été modifiée. 
  
Aucune valeur ne signifie que les deux versions, si elles existent ou existent déjà, ne peuvent pas être synchronisées. Une version a été supprimée ou modifiée de manière si radicale que la synchronisation n’est plus possible.
  
Une application cliente qui a modifié **PR_RTF_COMPRESSED** doit définir la valeur FALSE dans cette propriété pour forcer la synchronisation. Les magasins de messages rtF doivent effectuer la synchronisation à l’aide de **RTFSync** pendant un appel [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Les clients rtF doivent vérifier  le paramètre de PR_RTF_IN_SYNC avant de lire **PR_RTF_COMPRESSED** et appeler **d’abord RTFSync** si nécessaire. 
  
Si **PR_BODY** des modifications ont été apportées à autre chose que son espace blanc, la boutique de messages doit supprimer PR_RTF_IN_SYNC **pour** mettre fin à la synchronisation. 
  
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

