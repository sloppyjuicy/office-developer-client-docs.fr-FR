---
title: Propriété canonique PidTagAnr
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cd14d1b42603d81897f5bfeb177382d7e8941300
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571240"
---
# <a name="pidtaganr-canonical-property"></a>Propriété canonique PidTagAnr

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de chaîne à utiliser dans une restriction de propriété sur une table de contenu de conteneur de carnet d’adresses. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificateur :  <br/> |0x360C  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés n’appartiennent à aucun objet ; Il est fourni par les fournisseurs de carnet d’adresses dans les structures [SPropertyRestriction.](spropertyrestriction.md) Cette propriété contient une chaîne de résolution de nom ambigu (ANR) qui peut être testée par rapport à la table de contenu d’un conteneur de carnet d’adresses pour rechercher les destinataires de message correspondants. 
  
Les fournisseurs de carnets d’adresses correspondent à la valeur de **PR_ANR** et des propriétés associées par rapport à chaque entrée de la table des matières, à l’aide d’un algorithme de correspondance défini par le fournisseur. La ou les colonnes utilisées dans cette correspondance sont choisies par le fournisseur dans le cadre de l’algorithme. La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est la colonne la plus couramment utilisée ; la **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) est également utile lorsqu’elle contient le nom de messagerie de l’utilisateur. 
  
Pour plus d’informations sur la résolution de noms ambigus, voir [Restrictions du carnet d’adresses.](address-book-restrictions.md) 
  
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
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

