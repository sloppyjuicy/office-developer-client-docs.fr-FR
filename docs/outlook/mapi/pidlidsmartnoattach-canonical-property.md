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
ms.openlocfilehash: 7e6a736229a4e8b19886c41a68f89a8cc4ad1acf
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724532"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>Propriété canonique PidLidSmartNoAttach

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente si les pièces jointes d’un message sont considérées comme masquées.
  
|Propriété |Valeur |
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
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

