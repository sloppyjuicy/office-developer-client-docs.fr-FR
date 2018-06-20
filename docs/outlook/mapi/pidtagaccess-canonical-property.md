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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785662"
---
# <a name="pidtagaccess-canonical-property"></a>Propriété canonique PidTagAccess

  
  
**S’applique à**: Outlook 
  
Contient un masque de bits d’indicateurs indiquant les opérations qui sont disponibles pour le client de l’objet.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACCESS  <br/> |
|Identificateur :  <br/> |0x0FF4  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Propriétés de contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule pour le client. Il doit être un binaire **ou** de zéro ou plusieurs valeurs dans le tableau ci-après. 
  
|**Nom**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Écriture  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Lire  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0 x 00000004  <br/> |Suppression  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0 x 00000008  <br/> |Créer des sous-dossiers dans la hiérarchie de dossiers  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0 x 00000010  <br/> |Créer des messages de contenu  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0 x 00000020  <br/> |Créer des messages de contenu associés  <br/> |
   
Les indicateurs MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY et MAPI_ACCESS_READ sont trouvent dans le dossier et les objets de message et dans la colonne **PR_ACCESS** dans les tables des matières et contenu associé. Les indicateurs MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS et MAPI_ACCESS_CREATE_HIERARCHY sont trouvent sur des objets de dossier uniquement. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

