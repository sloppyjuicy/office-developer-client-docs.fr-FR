---
title: Propriété canonique PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6b16432fa09cf6fbece569bdf492915f735474c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620223"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a>Propriété canonique PidTagInitialDetailsPane

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique la page d’un modèle d’affichage à afficher en premier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INITIAL_DETAILS_PANE  <br/> |
|Identificateur :  <br/> |0x3F08  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tableaux d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Elle doit être présente sur tous les objets de carnet d’adresses sur un serveur NSPI (Name Service Provider Interface) et doit avoir la valeur zéro (0). Elle ne doit pas être définie pour les objets d’un carnet d’adresses en mode hors connexion.
  
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

