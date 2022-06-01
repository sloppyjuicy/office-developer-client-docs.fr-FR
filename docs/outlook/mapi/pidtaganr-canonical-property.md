---
title: PidTagAnr Canonical, propriété
description: Décrit la propriété canonique PidTagAnr, qui contient une valeur de chaîne à utiliser dans une restriction de propriété sur une table de contenu de conteneur de carnet d’adresses.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
ms.openlocfilehash: 18d7a9bafaedd775a19f8db65c5320ee92a96adc
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817339"
---
# <a name="pidtaganr-canonical-property"></a>PidTagAnr Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de chaîne à utiliser dans une restriction de propriété sur une table de contenu de conteneur de carnet d’adresses. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificateur :  <br/> |0x360C  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés n’appartiennent à aucun objet ; il est fourni par les fournisseurs de carnets d’adresses dans les structures [SPropertyRestriction](spropertyrestriction.md) . Cette propriété contient une chaîne de résolution de noms ambiguë (ANR) qui peut être testée sur la table de contenu d’un conteneur de carnet d’adresses pour rechercher les destinataires de messages correspondants. 
  
Les fournisseurs de carnets d’adresses correspondent à la valeur de **PR_ANR** et aux propriétés associées par rapport à chaque entrée de la table des matières, à l’aide d’un algorithme de correspondance défini par le fournisseur. La ou les colonnes utilisées dans cette correspondance sont choisies par le fournisseur dans le cadre de l’algorithme. La colonne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est la plus couramment utilisée ; La colonne **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) est également utile lorsqu’elle contient le nom de messagerie de l’utilisateur. 
  
Pour plus d’informations sur la résolution de noms ambigus, consultez [Restrictions du carnet d’adresses](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

