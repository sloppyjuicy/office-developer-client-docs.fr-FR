---
title: Propriété canonique PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786613"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Propriété canonique PidTagRoamingDatatypes

  
  
**S’applique à**: Outlook 
  
Contient un masque de bits indiquant le flux de propriétés existent sur le message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Identificateur :  <br/> |0x7C06  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Configuration  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie à une ou plusieurs des valeurs suivantes :
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000002  <br/> |Indique que le message du dossier associé informations (FAI) doit contenir un flux de dictionnaire, sérialisées dans un schéma XML fixe et stockées dans la propriété **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)). Si le message FAI ne contient pas un flux de dictionnaire, l’application doit traiter le dictionnaire qu’aucune entrée.  <br/> |
|0 x 00000004  <br/> |Indique que le message FAI doit contenir un flux de données XML stockée dans la propriété **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) qui utilise un schéma XML arbitraire.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

