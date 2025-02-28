---
title: PidTagGender Canonical, propriété
description: Cet article décrit la propriété canonique PidTagGender, qui contient le sexe de l’utilisateur de messagerie.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
ms.openlocfilehash: 57432592edbbb1a7598b286217db259e68363481
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769283"
---
# <a name="pidtaggender-canonical-property"></a>PidTagGender Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le sexe de l’utilisateur de messagerie.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_GENDER  <br/> |
|Identificateur :  <br/> |0x3A4D  <br/> |
|Type de données :  <br/> |PT_I2  <br/> |
|Domaine :  <br/> |Utilisateur de messagerie MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit des informations d’identification et d’accès sur un utilisateur de messagerie et le contenu. Le contenu est défini par l’utilisateur de messagerie et l’organisation de l’utilisateur de messagerie. 
  
Les valeurs possibles pour cette propriété sont définies dans l’énumération de genre. Elles sont répertoriées comme suit :
  
|**Énumération de genre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |Le sexe du contact n’est pas spécifié. |
|genderFemale  <br/> |0x0001  <br/> |Le contact est féminin. |
|genderMale  <br/> |0x0002  <br/> |Le contact est masculin. |
   
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
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

