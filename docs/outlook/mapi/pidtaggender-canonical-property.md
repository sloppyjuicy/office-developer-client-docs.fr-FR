---
title: Propriété canonique PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386613"
---
# <a name="pidtaggender-canonical-property"></a>Propriété canonique PidTagGender

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le sexe de l’utilisateur de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_GENDER  <br/> |
|Identificateur :  <br/> |0x3A4D  <br/> |
|Type de données :  <br/> |PT_I2  <br/> |
|Domaine :  <br/> |Utilisateur de messagerie MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit des informations d’identification et l’accès sur un utilisateur de messagerie et du contenu. Le contenu est défini par l’utilisateur de messagerie et l’organisation de messagerie de l’utilisateur. 
  
Les valeurs possibles pour cette propriété sont définies dans l’énumération sexe. Ils sont répertoriés comme suit :
  
|**Énumération sexe**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |Le sexe du contact n’est pas spécifié.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |Le contact est féminin.  <br/> |
|genderMale  <br/> |0x0002  <br/> |Le contact est masculin.  <br/> |
   
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

