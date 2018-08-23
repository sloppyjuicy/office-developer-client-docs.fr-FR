---
title: Propriété canonique PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6cc5edf1c93ca94fb9d8cab302ccd8e96373cd94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581943"
---
# <a name="pidtaganr-canonical-property"></a>Propriété canonique PidTagAnr

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une valeur de chaîne pour une utilisation dans une restriction de propriété sur une table des matières adresses livre conteneur. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificateur :  <br/> |0x360C  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés n’appartiennent pas à n’importe quel objet ; Il est fourni par les fournisseurs de carnet d’adresses dans des structures [SPropertyRestriction](spropertyrestriction.md) . Cette propriété contient une chaîne (ANR) de résolution de nom ambigu qui peut être testée par rapport à la table de contenu d’un conteneur carnet d’adresses pour rechercher les destinataires du message correspondant. 
  
Fournisseurs de carnet d’adresses correspondent à la valeur de **PR_ANR** et des propriétés associées par rapport à chaque entrée dans la table des matières, à l’aide d’un algorithme de correspondance défini par le fournisseur. L’ou les colonnes qui sont utilisés dans cette correspondance sont choisis par le fournisseur dans le cadre de l’algorithme. La colonne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est le plus fréquemment utilisée ; la colonne **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) est également utile lorsqu’il contient le nom de l’utilisateur de messagerie. 
  
Pour plus d’informations sur la résolution de nom ambigu, consultez [Restrictions de carnet d’adresses](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

