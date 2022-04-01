---
title: Propriété canonique PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d4641c72b70b7891cdb1cc8d1d3436fce1b1f168
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523579"
---
# <a name="pidtaginconflict-canonical-property"></a>Propriété canonique PidTagInConflict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE lorsque la pièce jointe représente un autre réplica.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IN_CONFLICT  <br/> |
|Identificateur :  <br/> |0x666C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Note de conflit  <br/> |
   
## <a name="remarks"></a>Remarques

Le client et le serveur de messagerie doivent générer un message de résolution de conflit lors de la détection d’un conflit avec la version actuelle d’un message dans le réplica lors de la synchronisation. Il est important de comprendre qu’il est possible que la version actuelle du message dans le réplica local a été transmise pendant l’opération de synchronisation en cours. Cela se produit lorsque le conflit existe déjà sur le serveur avant le téléchargement de l’un des messages en conflit vers le réplica local. Un message de résolution de conflit doit être synchronisé en tant que réplicas indépendants avec des PCL en conflit. Le message de résolution de conflit lui-même ne doit pas être synchronisé entre le client et le serveur ; seuls les réplicas indépendants doivent être échangés. Le partenaire de synchronisation doit ensuite générer un nouveau message qui correspond à la structure du message en conflit. Par conséquent, il est important que le client et le serveur utilisent le même algorithme pour détecter l’élément « gagne ». Les règles suivantes doivent être appliquées pour détecter le « gagneur » :
  
1. Heure de la dernière modification.
    
2. GUID CN supérieur (à l’aide de la comparaison de mémoire) pour rompre l’égalité.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

