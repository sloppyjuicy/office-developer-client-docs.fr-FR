---
title: Propriété canonique PidTagAccessLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: Indique le niveau d’accès du client à l’objet. Cette propriété est en lecture seule pour le client.
ms.openlocfilehash: b17bfa733783b31f48fbd9485eea176fae78eb89
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405719"
---
# <a name="pidtagaccesslevel-canonical-property"></a>Propriété canonique PidTagAccessLevel

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le niveau d’accès du client à l’objet.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACCESS_LEVEL  <br/> |
|Identificateur :  <br/> |0x0FF7  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Propriétés du contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule pour le client. Elle doit avoir l’une des valeurs suivantes :
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Lecture seule  <br/> |
|0x00000001  <br/> |Modifier  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
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

