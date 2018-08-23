---
title: Propriété canonique PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 33bf77029207e2d8d734d5c49735262135896660
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593724"
---
# <a name="pidtaginconflict-canonical-property"></a>Propriété canonique PidTagInConflict

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE lorsque la pièce jointe représente un autre réplica.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IN_CONFLICT  <br/> |
|Identificateur :  <br/> |0x666C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Note de conflit  <br/> |
   
## <a name="remarks"></a>Remarques

Le client de messagerie et le serveur doivent générer un message de résolution de conflit lors de la détection de conflit par rapport à la version actuelle d’un message dans le réplica lors de la synchronisation. Il est important de comprendre qu’il est possible que la version actuelle du message dans le réplica local a été transmise au cours de l’opération en cours de synchronisation. Cela se produit lorsque le conflit existe déjà sur le serveur avant d’un des messages en conflit ont été téléchargé sur le réplica local. Un conflit de résoudre le message doit être synchronisé en tant que réplicas indépendants avec PCLs en conflit. Résoudre le conflit le message lui-même ne doit pas être synchronisée entre client et serveur ; uniquement les réplicas indépendantes doivent être échangés. Le partenaire de synchronisation doit ensuite générer un nouveau message qui correspond à la structure du message de conflit. Par conséquent, il est important que client et serveur utilisent le même algorithme pour détecter l’élément « prix ». Les règles suivantes doivent être appliquées pour détecter le « prix » :
  
1. Heure de dernière modification.
    
2. Supérieur CN GUID (à l’aide de la comparaison de la mémoire) pour rompre papillon.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

