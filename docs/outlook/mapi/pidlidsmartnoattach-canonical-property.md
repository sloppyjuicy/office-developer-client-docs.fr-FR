---
title: Propriété canonique PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 43e10652a7dccdf0da6592df0f9fc2daf5ea9bee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785412"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>Propriété canonique PidLidSmartNoAttach

  
  
**S’applique à**: Outlook 
  
Indique si les pièces jointes d’un message sont considérés comme étant masquées.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSmartNoAttach  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008514  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Configuration d’exécution  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a la valeur TRUE si les pièces jointes du message sont considérés comme étant masquées.
  
Il indique si l’objet message n’a pas les pièces jointes visible pour l’utilisateur final. Cette propriété peut être annulée ; Dans ce cas, la valeur FALSE par défaut est supposée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

