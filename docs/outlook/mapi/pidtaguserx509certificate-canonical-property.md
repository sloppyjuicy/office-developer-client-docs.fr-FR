---
title: Propriété canonique PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 48b3a895c13ec2838994972e17ccabc29bed1d1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578913"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>Propriété canonique PidTagUserX509Certificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des certificats de sécurité X.509 version 3 pour un utilisateur de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x3A70  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Utilisateur de messagerie MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée par les applications qui utilisent la sécurité à clé publique. Il contient une représentation binaire d’un ou de plusieurs certificats de sécurité X.509 version 3. 
  
Diverses applications et clients peuvent utiliser cette propriété pour leurs propres certificats de sécurité. Le format binaire des données X.509 peut varier d’un fournisseur à l’autre. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
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

