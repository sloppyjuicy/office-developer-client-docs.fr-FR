---
title: Propriété canonique PidTagLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLocation
api_type:
- HeaderDef
ms.assetid: 99dffcd9-83dc-462e-b0ce-e2101e546cc6
description: Contient l’emplacement du destinataire dans un format utile pour l’organisation du destinataire. Ces propriétés sont définies par le destinataire et son organisation.
ms.openlocfilehash: 5d8b2708cb87bc0834798614356cbdd4c6c71292
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763760"
---
# <a name="pidtaglocation-canonical-property"></a>Propriété canonique PidTagLocation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’emplacement du destinataire dans un format utile pour l’organisation du destinataire. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LOCATION, PR_LOCATION_A, PR_LOCATION_W  <br/> |
|Identificateur :  <br/> |0x3A0D  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés fournissent des informations d’identification et d’accès pour un destinataire. Elles sont définies par le destinataire et leur organisation. 
  
Le contenu est défini par les besoins de l’organisation du destinataire. Par exemple, certaines organisations peuvent identifier les utilisateurs de messagerie en spécifiant le numéro de bâtiment et le numéro de bureau. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
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

