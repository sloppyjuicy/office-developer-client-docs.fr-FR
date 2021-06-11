---
title: Propriété canonique PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316512"
---
# <a name="pidtagaccess-canonical-property"></a>Propriété canonique PidTagAccess

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs indiquant les opérations disponibles pour le client pour l’objet.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACCESS  <br/> |
|Identificateur :  <br/> |0x0FF4  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Propriétés du contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule pour le client. Il doit s’agit d’un **OR** au niveau du bit de zéro ou de plusieurs valeurs du tableau suivant. 
  
|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Write  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Lecture  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Supprimer  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Créer des sous-dossiers dans la hiérarchie de dossiers  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Créer des messages de contenu  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Créer des messages de contenu associés  <br/> |
   
Les indicateurs MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY et MAPI_ACCESS_READ sont trouvés sur les objets de dossier et de message, ainsi que dans la colonne **PR_ACCESS** des tables des matières et des tables des matières associées. Les indicateurs MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS et MAPI_ACCESS_CREATE_HIERARCHY sont trouvés uniquement sur les objets de dossier. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

