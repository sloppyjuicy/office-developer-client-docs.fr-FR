---
title: Propriété canonique PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385535"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>Propriété canonique PidTagUserX509Certificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les certificats de sécurité X.509 version 3 pour un utilisateur de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x3A70  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Utilisateur de messagerie MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée par les applications qui utilisent la sécurité de clé publique. Il conserve une représentation binaire d’un ou plusieurs certificats de sécurité 3 X.509 version. 
  
Des clients et des applications différentes peuvent utiliser cette propriété leurs propres certificats de sécurité. Le format des données X.509 binaire peut varier entre fournisseurs. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
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

