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
ms.openlocfilehash: 27e3a9687d66bd1cd3586a25a3ca5792523096c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785960"
---
# <a name="pidtagemsabserver-canonical-property"></a>Propriété canonique PidTagEmsAbServer

  
  
**S’applique à**: Outlook 
  
Spécifie le chemin d’accès d’un conteneur de carnet d’adresses dans un scénario en mode hors connexion ou le nom de domaine complet du serveur de catalogue global où le conteneur de carnet d’adresses se trouve dans un scénario en ligne.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Identificateur :  <br/> |0xFFFE  <br/> |
|Type de données :  <br/> |PT_TSTRING  <br/> |
|Zone :  <br/> |Carnet d'adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est le type de propriété rétablir **PT_UNICODE** lorsqu’il est compilé avec la `UNICODE` symbole sur une plateforme Unicode et **PT_STRING8** lorsqu’il n’est pas compilé avec la `UNICODE` symbole. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

