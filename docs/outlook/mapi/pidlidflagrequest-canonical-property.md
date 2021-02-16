---
title: Propriété canonique PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357805"
---
# <a name="pidlidflagrequest-canonical-property"></a>Propriété canonique PidLidFlagRequest

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente l’état d’une demande de réunion.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidRequest  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008530  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Marquage  <br/> |
   
## <a name="remarks"></a>Remarques

Dans Microsoft Office Outlook, une demande de réunion est un élément de rendez-vous.
  
Cette propriété contient le texte spécifié par l’utilisateur à associer à l’indicateur et doit être définie si l’objet message est marqué ou terminé, mais qu’il ne doit pas exister pour un objet lié à une réunion. Les clients peuvent choisir de ne pas prendre en charge cette propriété et toujours écrire « Suivi » (traduit dans la langue de l’utilisateur, le cas échéant) comme valeur de la chaîne lorsque cette propriété doit être définie. Cette propriété doit être ignorée de manière conditionnée en fonction des valeurs des propriétés **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) et **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

