---
title: Propriété canonique PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335797"
---
# <a name="pidtagemsabserver-canonical-property"></a>Propriété canonique PidTagEmsAbServer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le chemin d'accès d'un conteneur de carnet d'adresses dans un scénario hors connexion ou le nom de domaine complet du serveur de catalogue global où le conteneur de carnet d'adresses réside dans un scénario en ligne.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Identificateur :  <br/> |0xFFFE  <br/> |
|Type de données :  <br/> |PT_TSTRING  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a le type de propriété Reset à **PT_UNICODE** lorsqu'elle est compilée `UNICODE` avec le symbole sur une plateforme Unicode, et à **PT_STRING8** lorsqu'elle n'est pas `UNICODE` compilée avec le symbole. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

