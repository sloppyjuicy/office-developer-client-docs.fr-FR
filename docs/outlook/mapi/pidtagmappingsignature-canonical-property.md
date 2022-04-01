---
title: Propriété canonique PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e961cf883b628a9f644124f15c0916c188fabbd7
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524347"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Propriété canonique PidTagMappingSignature

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la signature de mappage pour les propriétés nommées d’un objet MAPI particulier. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Identificateur :  <br/> |0x0FF8  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets ayant des propriétés nommées exposent cette propriété. Une application cliente doit vérifier la **propriété PR_MAPPING_SIGNATURE** des deux objets lors de la copie des propriétés nommées d’un objet à un autre. L’utilisation de cette propriété peut réduire la traduction entre les noms et les identificateurs des propriétés copiées. 
  
Si cette propriété n’existe pas pour un objet MAPI donné, l’objet possède son propre mappage unique de noms et d’identificateurs. Dans ce cas, le client doit appeler la méthode [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) sur l’objet source, puis la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) sur l’objet de destination. 
  
Lorsque deux objets ont la même valeur **PR_MAPPING_SIGNATURE** , le client n’a pas besoin de traduire le nom en identificateur et identificateur en nom. Le client peut simplement appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) sur la source, puis la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) sur la destination. Cela est pratique pour les clients qui effectuent une copie personnalisée des propriétés nommées et pour les fournisseurs implémentant les méthodes [IMAPIProp::CopyTo](imapiprop-copyto.md) et [IMAPIProp::CopyProps](imapiprop-copyprops.md) . 
  
Pour plus d’informations sur les propriétés nommées et le mappage des noms et des identificateurs, voir [PROPRIÉTÉS nommées MAPI](mapi-named-properties.md). 
  
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



[MAPINAMEID](mapinameid.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

