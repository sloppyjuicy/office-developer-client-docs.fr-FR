---
title: PidTagAssistantTelephoneNumber, propriété canonique
description: Décrit la propriété canonique PidTagAssistantTelephoneNumber, qui contient le numéro de téléphone de l’assistant administratif du destinataire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAssistantTelephoneNumber
api_type:
- HeaderDef
ms.assetid: edb0782c-6671-4e98-9028-a2f9ad547c1d
ms.openlocfilehash: e900b90666f22c42a05a1bca0744c7fd863482c2
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811927"
---
# <a name="pidtagassistanttelephonenumber-canonical-property"></a>PidTagAssistantTelephoneNumber, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le numéro de téléphone de l’assistant administratif du destinataire. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ASSISTANT_TELEPHONE_NUMBER, PR_ASSISTANT_TELEPHONE_NUMBER_A, PR_ASSISTANT_TELEPHONE_NUMBER_W  <br/> |
|Identificateur :  <br/> |0x3A2E  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés fournissent des informations d’identification et d’accès pour un destinataire. Elles sont définies par le destinataire et son organisation. 
  
Le numéro de téléphone correspond à l’assistant spécifié dans la propriété **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

