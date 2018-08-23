---
title: Propriété canonique PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1f528332c52664ac472670566c905d36dac65bfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565528"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Propriété canonique PidNameRightsManagementLicense

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Met en cache de la licence d’utilisation pour le message électronique géré par des droits.
  
|||
|:-----|:-----|
|Noms conviviaux :  <br/> |Aucun  <br/> |
|Jeu de propriétés :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nom de la propriété :  <br/> |DRMLicense  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Messagerie sécurisée  <br/> |
   
## <a name="remarks"></a>Remarques

Si la propriété est présente dans un message électronique géré par des droits, la première valeur de cette propriété binaire plusieurs doit contenir la licence d’utilisation compressé ZLIB (comme spécifié dans [RFC1950]) pour le message électronique géré par des droits.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages codés géré par des droits.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

