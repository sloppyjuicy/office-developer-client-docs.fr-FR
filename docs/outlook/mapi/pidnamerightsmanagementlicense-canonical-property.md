---
title: Propriété canonique PidNameRightsManagementLicense
description: Décrit la propriété canonique PidNameRightsManagementLicense, qui met en cache la licence d’utilisation pour le message électronique géré par les droits.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
ms.openlocfilehash: 4c57f96c0fa194e4fe3e61093335c6c9ca8493e8
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812600"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Propriété canonique PidNameRightsManagementLicense

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met en cache la licence d’utilisation pour le message électronique géré par des droits.
  
|Propriété |Valeur |
|:-----|:-----|
|Noms conviviaux :  <br/> |Aucun  <br/> |
|Jeu de propriétés :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nom de la propriété :  <br/> |DRMLicense  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Messagerie sécurisée  <br/> |
   
## <a name="remarks"></a>Remarques

Si la propriété est présente sur un message électronique géré par des droits, la première valeur de cette propriété binaire multiple doit contenir la licence d’utilisation compressée ZLIB (comme spécifié dans [RFC1950]) pour le message électronique géré par les droits.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages encodés gérés par des droits.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

