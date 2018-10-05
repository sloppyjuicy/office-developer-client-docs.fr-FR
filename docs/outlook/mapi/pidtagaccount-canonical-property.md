---
title: Propriété canonique PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401103"
---
# <a name="pidtagaccount-canonical-property"></a>Propriété canonique PidTagAccount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom du compte du destinataire. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W  <br/> |
|Identificateur :  <br/> |0x3A00  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés permettent d’identifier et accéder aux informations pour un destinataire. Ils sont définis par le destinataire et de leur organisation.
  
Ces propriétés couramment contiennent du nom de messagerie du destinataire, autrement dit, le dernier composant de l’adresse de messagerie, qui identifie le destinataire dans l’organisation locale. L’adresse de messagerie correspond au nom unique X.400, qui est supposé être un nom court uniques au sein d’un certain domaine de messagerie.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

