---
title: PidLidWhere Canonical, propriété
description: Décrit la propriété canonique PidLidWhere, qui spécifie l’emplacement d’un événement et s’applique à Outlook 2013 et Outlook 2016.
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
ms.openlocfilehash: cc1293c005be57fa2bdc62ebacf47165ecb0d4c8
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816051"
---
# <a name="pidlidwhere-canonical-property"></a>PidLidWhere Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’emplacement d’un événement.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |LID_WHERE  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID long (LID) :  <br/> |0x00000002  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être identique à la valeur de la propriété **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) de la réunion associée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

