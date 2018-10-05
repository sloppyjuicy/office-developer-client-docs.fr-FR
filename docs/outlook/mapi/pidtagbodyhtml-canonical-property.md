---
title: Propriété canonique PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384968"
---
# <a name="pidtagbodyhtml-canonical-property"></a>Propriété canonique PidTagBodyHtml

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la version de langage HTML (Hypertext Markup) du texte du message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W  <br/> |
|Identificateur :  <br/> |0x1013  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent le texte du message même en tant que la **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mais dans le code HTML. 
  
Une banque de messages qui prend en charge HTML indique qu’il en définissant l’indicateur **STORE_HTML_OK** dans son **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
 **Remarque** **STORE_HTML_OK** n’est pas défini dans les versions de Mapidefs.h inclus avec Microsoft® Exchange Server 2000 et versions antérieures. Si **STORE_HTML_OK** n’est pas défini, utilisez plutôt la valeur 0 x 00010000. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

