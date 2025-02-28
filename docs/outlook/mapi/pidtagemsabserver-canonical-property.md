---
title: Propriété canonique PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: Spécifie le chemin d’accès d’un conteneur de carnet d’adresses (hors connexion) ou le nom de domaine du serveur de catalogue global où réside le conteneur de carnet d’adresses, en ligne.
ms.openlocfilehash: 1cb742d35fae312d1e492ca96d028b50a88bdec1
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763102"
---
# <a name="pidtagemsabserver-canonical-property"></a>Propriété canonique PidTagEmsAbServer

**S’applique à** : Outlook 2013 | Outlook 2016
  
Spécifie le chemin d’accès d’un conteneur de carnet d’adresses dans un scénario hors connexion ou le nom de domaine complet du serveur de catalogue global où réside le conteneur de carnet d’adresses dans un scénario en ligne.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Identificateur :  <br/> |0xFFFE  <br/> |
|Type de données :  <br/> |PT_TSTRING  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |

## <a name="remarks"></a>Remarques

Cette propriété a le type de propriété réinitialisé à **PT_UNICODE**  `UNICODE` lorsqu’elle est compilée avec le symbole sur une plateforme Unicode et à **PT_STRING8**  `UNICODE` lorsqu’elle n’est pas compilée avec le symbole.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.

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
