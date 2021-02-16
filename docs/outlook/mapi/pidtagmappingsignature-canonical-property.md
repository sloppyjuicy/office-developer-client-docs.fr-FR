---
title: Propriété canonique PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342538"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Propriété canonique PidTagMappingSignature

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la signature de mappage pour les propriétés nommées d’un objet MAPI particulier. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Identificateur :  <br/> |0x0FF8  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets ayant des propriétés nommées exposent cette propriété. Une application cliente doit vérifier la **propriété PR_MAPPING_SIGNATURE** des deux objets lors de la copie des propriétés nommées d’un objet à un autre. L’utilisation de cette propriété peut réduire la traduction entre les noms et les identificateurs des propriétés copiées. 
  
Si cette propriété n’existe pas pour un objet MAPI donné, l’objet possède son propre mappage unique de noms et d’identificateurs. Dans ce cas, le client doit appeler la méthode [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) sur l’objet source, puis la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) sur l’objet de destination. 
  
Lorsque deux objets ont la même valeur **PR_MAPPING_SIGNATURE,** le client n’a pas besoin de traduire le nom en identificateur et identificateur en nom. Le client peut simplement appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) sur la source, puis la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) sur la destination. Cela est pratique pour les clients qui effectuent une copie personnalisée des propriétés nommées et pour les fournisseurs implémentant les méthodes [IMAPIProp::CopyTo](imapiprop-copyto.md) et [IMAPIProp::CopyProps.](imapiprop-copyprops.md) 
  
Pour plus d’informations sur les propriétés nommées et le mappage des noms et des identificateurs, voir [MAPI Named Properties](mapi-named-properties.md). 
  
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



[MAPINAMEID](mapinameid.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

