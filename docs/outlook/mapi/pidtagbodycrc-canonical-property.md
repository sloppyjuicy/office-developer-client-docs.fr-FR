---
title: Propriété canonique PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: Contient une valeur de vérification de redondance cyclique (CRC) sur le texte du message. La magasin de messages peut utiliser n’importe quel algorithme CRC qui génère une PT_LONG valeur.
ms.openlocfilehash: 5d4a66b71cd04fca5ae493d7186561d9c871ca6a
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762262"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propriété canonique PidTagBodyCrc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de vérification de redondance cyclique (CRC) sur le texte du message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY_CRC  <br/> |
|Identificateur :  <br/> |0x0E1C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

La magasin de messages peut utiliser n’importe quel algorithme CRC qui génère une PT_LONG valeur. Elle doit calculer cette propriété dans le cadre de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) lorsque la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) a été définie pour la première fois et chaque fois qu’elle a été modifiée par la suite.
  
Une application cliente utilise **PR_BODY_CRC** pour vous aider à comparer les chaînes de texte de message contenues **dans PR_BODY** propriétés ou leurs variantes. À l’aide de cette propriété, le client peut rapidement et facilement détecter si le texte du message a changé. Il peut réaliser des gains de performances significatifs en utilisant **PR_BODY_CRC** au lieu d’obtenir des  PR_BODY dans la boutique de messages et de les comparer à une version locale. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

