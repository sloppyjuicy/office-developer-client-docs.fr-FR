---
title: Propriété canonique PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f73e45038aac9da37519440efce38a4085f83cf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630186"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>Propriété canonique PidLidSmartNoAttach

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente si les pièces jointes d’un message sont considérées comme masquées.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSmartNoAttach  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008514  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Configuration au moment de l’exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a la valeur TRUE si les pièces jointes du message sont considérées comme masquées.
  
Il indique si l’objet message ne possède pas de pièces jointes visibles par l’utilisateur final. Cette propriété peut être non jeu ; si c’est le cas, une valeur par défaut de FALSE est supposée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

