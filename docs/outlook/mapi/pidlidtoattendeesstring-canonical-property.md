---
title: Propriété canonique PidLidToAttendeesString
description: Décrit la propriété canonique PidLidToAttendeesString, qui contient une liste de tous les participants expéditeurs qui sont également des participants requis.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
ms.openlocfilehash: e87c13449e5e6ec7f9c2232c51191e000d685cdb
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817388"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a>Propriété canonique PidLidToAttendeesString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la liste de tous les participants pouvant être envoyés qui sont également des participants requis.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidToAttendeesString  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x0000823B  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d’adresses du participant. Les entrées distinctes doivent être délimitées par un point-virgule suivi d’un espace. Cette propriété n’est pas obligatoire.
  
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

