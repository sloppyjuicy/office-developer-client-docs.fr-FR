---
title: Propriété canonique PidTagTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2501ea7c4be08b0bec3c2d65e6a504df47dfc488
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388279"
---
# <a name="pidtagtitle-canonical-property"></a>Propriété canonique PidTagTitle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la fonction du destinataire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TITLE, PR_TITLE_A, PR_TITLE_W  <br/> |
|Identificateur :  <br/> |0x3A17  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Utilisateur de messagerie MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés permettent d’identifier et accéder aux informations pour un destinataire. Ils sont définis par le destinataire et l’organisation du destinataire. 
  
Ces propriétés sont généralement utilisées pour indiquer le titre du destinataire formels de travail, tels que le programmeur Senior, plutôt que la classe professionnelle, comme le programmeur. Il n’est pas généralement utilisé pour les titres de « suffixe » comme esq ou partage dynamique de lecteurs.
  
Incluent des valeurs communes pour cette propriété : directeur, programmeur II, professeur et responsable du développement. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
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

