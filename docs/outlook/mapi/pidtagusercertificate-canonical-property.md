---
title: Propriété canonique PidTagUserCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: Contient un certificat d’authentification ASN.1 pour un utilisateur de messagerie pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 0c7cf93cf57c3cba061a7282784abd2e8a2cec83
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455670"
---
# <a name="pidtagusercertificate-canonical-property"></a>Propriété canonique PidTagUserCertificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un certificat d’authentification ASN.1 pour un utilisateur de messagerie. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_USER_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x3A22  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Utilisateur de messagerie MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un certificat d’authentification est similaire à une signature numérique. Plusieurs propriétés MAPI fournissent des certificats ASN.1. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

